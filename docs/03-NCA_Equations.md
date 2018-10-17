# Equations



For the parameter table below, concentrations measured below the limit of concentration are assumed to be written as zero.  Also, mathematical terminology differs in many references; throughout this document, $ln$ is used to indicate the natural logarithm (also known as the logarithm base $e$, $log_e$, and ${}^elog$).

## Defined Parameters

The following parameter definitions are used throughout the parameter table, and these parameters are defined parameter (not calculated).


------------------------------------------
 Symbol       Units         Definition    
-------- --------------- -----------------
   C      concentration    Concentration  

   D         amount            Dose       

   t          time             Time       

 $\tau$       time        Dosing interval 
------------------------------------------


## Parameter Table






-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
             symbol                       units                     definition                         cdisc               single   multiple   intravenous   extravascular                          equation                                        notes                  reference 
-------------------------------- ----------------------- -------------------------------- ------------------------------- -------- ---------- ------------- --------------- -------------------------------------------------------- ------------------------------------ -----------
           $C_{max}$                  concentration         The maximum concentration                  CMAX                 TRUE      TRUE        TRUE           TRUE                               Observed                                                                         
                                                             occurring at $t_{max}$.                                                                                                                                                                                                 

           $t_{max}$                      time                The time of $C_{max}$.                   TMAX                 TRUE      TRUE        TRUE           TRUE                               Observed                                                                         

           $C_{min}$                  concentration         The minimum concentration                  CMIN                 TRUE      TRUE        TRUE           TRUE                               Observed                                    [1][$C_{min}$]                       
                                                           occurring between dose time                                                                                                                                                                                               
                                                          and dose time plus $\tau$ (at                                                                                                                                                                                              
                                                                   $t_{min}$).                                                                                                                                                                                                       

           $t_{min}$                      time                The time of $C_{min}$.                   TMIN                 TRUE      TRUE        TRUE           TRUE                               Observed                                                                         

          $C_{trough}$                concentration       Concentration at end of dosing              CTROUGH               TRUE      TRUE        TRUE           TRUE                               Observed                                  [2][$C_{trough}$]                      
                                                                    interval.                                                                                                                                                                                                        

           $t_{lag}$                      time             The time prior to the first                 TLAG                 TRUE      TRUE        TRUE           TRUE                               Observed                                                               (, 2013)  
                                                            increase in concentration.                                                                                                                                                                                               

         $C_{last,obs}$               concentration             The last observed                      CLST                 TRUE      TRUE        TRUE           TRUE                               Observed                                                               (, 2013)  
                                                          concentration above the limit                                                                                                                                                                                              
                                                                of quantification.                                                                                                                                                                                                   
                                                                Equivalently, the                                                                                                                                                                                                    
                                                          concentration corresponding to                                                                                                                                                                                             
                                                                   $t_{last}$.                                                                                                                                                                                                       

        $C_{last,pred}$               concentration            The concentration at                                         TRUE      TRUE        TRUE           TRUE                     $$C_{last,pred} = \lambda_z                        [3][$C_{last,pred}$]          (, 2013)  
                                                          $t_{last}$ predicted from the                                                                                                      \times t_{last} + A$$                                                                   
                                                           log-linear regression of the                                                                                                                                                                                              
                                                               terminal part of the                                                                                                                                                                                                  
                                                           concentration-time curve (as                                                                                                                                                                                              
                                                            estimated for half-life).                                                                                                                                                                                                

           $t_{last}$                     time                 The time of the last                    TLST                 TRUE      TRUE        TRUE           TRUE                               Observed                                                               (, 2013)  
                                                              measurable (positive)                                                                                                                                                                                                  
                                                                  concentration.                                                                                                                                                                                                     

       $AUC_{a,b,linear}$          concentration*time      Area under the concentration                                     TRUE      TRUE        TRUE           TRUE                        $$AUC_{t_i,t_{i+1}} =                                                         (, 2013)  
                                                          time curve from measurement at                                                                                                    \frac{1}{2} \left(C_i +                                                                  
                                                          time $a$ to time $b$ using the                                                                                                 C_{i+1}\right) \left(t_{i+1} -                                                              
                                                             linear trapezoidal rule.                                                                                                             t_i\right)$$                                                                       

     $AUC_{a,b,log-linear}$        concentration*time      Area under the concentration                                     TRUE      TRUE        TRUE           TRUE                        $$AUC_{t_i,t_{i+1}} =                                                         (, 2013)  
                                                          time curve from measurement at                                                                                                       \frac{\left(C_i -                                                                     
                                                          time $a$ to time $b$ using the                                                                                                 C_{i+1}\right) \left(t_{i+1} -                                                              
                                                           log-linear trapezoidal rule.                                                                                                      t_i\right)}{ln{C_i} -                                                                   
                                                                                                                                                                                                 ln{C_{i+1}}}$$                                                                      

   $AUC_{0,t}$, $AUC_{last}$,      concentration*time      Area under the concentration       AUCINT, AUCLST, AUCTAU        TRUE      TRUE        TRUE           TRUE                               $$AUC =                             [4][$AUC_{0,t}$, $AUC_{last}$,     (, 2013)  
          $AUC_{\tau}$                                     time curve during a defined                                                                                                    \sum_{t=a}^{t=min(t_{last},                           $AUC_{\tau}$]                        
                                                           interval using only samples                                                                                                      b)} AUC_{t_i,t_{i+1}}$$                                                                  
                                                                above the limit of                                                                                                                                                                                                   
                                                                  quantification                                                                                                                                                                                                     

 $AUC_{t_{last}-\infty,pred}$,     concentration*time             Area under the                                            TRUE      TRUE        TRUE           TRUE                    $$\frac{C_{last}}{\lambda_z}$$               [5][$AUC_{t_{last}-\infty,pred}$,    (, 2013)  
  $AUC_{t_{last}-\infty,obs}$                             concentration-time curve from                                                                                                                                                  $AUC_{t_{last}-\infty,obs}$]                
                                                              $t_{last}$ to $\infty$                                                                                                                                                                                                 

  $AUC_{t_{last}-\infty,all}$      concentration*time             Area under the                                            TRUE      TRUE        TRUE           TRUE                 $$AUC_{t_{last},t_{last+1},linear}$$             [6][$AUC_{t_{last}-\infty,all}$]    (, 2013)  
                                                          concentration-time curve from                                                                                                                                                                                              
                                                          $t_{last}$ to $\infty$ as used                                                                                                                                                                                             
                                                                 for $AUC_{all}$.                                                                                                                                                                                                    

     $AUC_{0-\infty,pred}$,        concentration*time     The area under the curve (AUC)          AUCIFP, AUCIFO            TRUE     FALSE        TRUE           TRUE                            $$AUC_{last} +                           [7][$AUC_{0-\infty,pred}$,       (, 2013)  
      $AUC_{0-\infty,obs}$                                  extrapolated to $\infty$,                                                                                                       AUC_{t_{last}-\infty}$$                         $AUC_{0-\infty,obs}$]                    
                                                          calculated using the observed                                                                                                                                                                                              
                                                          or predicted value of the last                                                                                                                                                                                             
                                                             non-zero concentration.                                                                                                                                                                                                 

         $AUC_{0,all}$             concentration*time     The area under the curve (AUC)              AUCALL                TRUE      TRUE        TRUE           TRUE                            $$AUC_{last} +                               [8][$AUC_{0,all}$]           (, 2013)  
                                                          from the time of dosing to the                                                                                                  AUC_{t_{last}-\infty,all}$$                                                                
                                                          time of the last observation,                                                                                                                                                                                              
                                                          regardless of whether the last                                                                                                                                                                                             
                                                          concentration is measurable or                                                                                                                                                                                             
                                                                       not.                                                                                                                                                                                                          

     $AUC_{\%extrap,obs}$,                  %             The area under the curve (AUC)          AUCPEO, AUCPEP            TRUE     FALSE        TRUE           TRUE            $$\frac{AUC_{t_{last},\infty}}{AUC_{0,\infty}}           [9][$AUC_{\%extrap,obs}$,        (, 2013)  
     $AUC_{\%extrap,pred}$                                    from the last observed                                                                                                                 \times                                 $AUC_{\%extrap,pred}$]                   
                                                           non-zero concentration value                                                                                                              100$$                                                                           
                                                          to infinity as a percentage of                                                                                                                                                                                             
                                                             the area under the curve                                                                                                                                                                                                
                                                          extrapolated to infinity using                                                                                                                                                                                             
                                                              either the observed or                                                                                                                                                                                                 
                                                              predicted $C_{last}$.                                                                                                                                                                                                  

              $F$                       fraction                 Bioavailability                                            TRUE     FALSE        TRUE           TRUE            $$\frac{AUC_{0,\infty,ev}}{AUC_{0,\infty,iv}}                    [10][$F$]                (, 2013)  
                                                                                                                                                                                            \frac{D_{iv}}{D_{ev}}$$                                                                  
                                                                                                                                                                             $$\frac{AUC_{0,\infty,test}}{AUC_{0,\infty,reference}}                                                  
                                                                                                                                                                                        \frac{D_{reference}}{D_{test}}$$                                                             

      $AUMC_{a,b,linear}$         concentration*time^2^   Area under the first moment of                                    TRUE      TRUE        TRUE           TRUE                    $$AUMC_{t_i,t_{i+1},linear} =                                                     (, 2013)  
                                                           the concentration time curve                                                                                                   \frac{1}{2} \left(t_{i+1} -                                                                
                                                           from measurement at time $a$                                                                                                    t_{i}\right) \left(C_{i+1}                                                                
                                                           to time $b$ using the linear                                                                                                    t_{i+1} + C_i t_i\right)$$                                                                
                                                                trapezoidal rule.                                                                                                                                                                                                    

    $AUMC_{a,b,log-linear}$       concentration*time^2^   Area under the first moment of                                    TRUE      TRUE        TRUE           TRUE                   $$AUMC_{t_i,t_{i+1},log-linear}                                                    (, 2013)  
                                                           the concentration time curve                                                                                                                =                                                                             
                                                           from measurement at time $a$                                                                                                         \frac{t_{i+1} -                                                                      
                                                              to time $b$ using the                                                                                                       t_{i}}{ln\left(C_i\right) -                                                                
                                                           log-linear trapezoidal rule.                                                                                                     ln\left(C_{i+1}\right)}                                                                  
                                                                                                                                                                                         \left(C_{i+1} \times t_{i+1} +                                                              
                                                                                                                                                                                           C_i \times t_i\right) + \\                                                                
                                                                                                                                                                                             \left(\frac{t_{i+1} -                                                                   
                                                                                                                                                                                          t_{i}}{ln\left(C_i\right) -                                                                
                                                                                                                                                                                        ln\left(C_{i+1}\right)}\right)^2                                                             
                                                                                                                                                                                          \left(C_i - C_{i+1}\right)$$                                                               

  $AUMC_{0,t}$, $AUMC_{last}$,    concentration*time^2^   Area under the first moment of         AUMCLST, AUMCTAU           TRUE      TRUE        TRUE           TRUE                           $$AUMC_{last} =                               [11][$AUMC_{0,t}$,           (, 2013)  
         $AUMC_{\tau}$                                     the concentration time curve                                                                                                   \sum_{t=a}^{t=min(t_{last},                   $AUMC_{last}$, $AUMC_{\tau}$]                
                                                            during a defined interval                                                                                                       b)} AUMC_{t_i,t_{i+1}}$$                                                                 
                                                           using only samples above the                                                                                                                                                                                              
                                                             limit of quantification                                                                                                                                                                                                 

 $AUMC_{t_{last}-\infty,obs}$,    concentration*time^2^   Area under the first moment of                                    TRUE      TRUE        TRUE           TRUE                           $$\frac{C_{last}                      [12][$AUMC_{t_{last}-\infty,obs}$,   (, 2013)  
 $AUMC_{t_{last}-\infty,pred}$                             the concentration-time curve                                                                                                      t_{last}}{\lambda_z} +                     $AUMC_{t_{last}-\infty,pred}$]               
                                                           from $t_{last}$ to $\infty$                                                                                                   \frac{C_{last}}{\lambda_z^2}$$                                                              

  $AUMC_{t_{last}-\infty,all}$    concentration*time^2^   Area under the first moment of                                    TRUE      TRUE        TRUE           TRUE                 $$AUC_{t_{last},t_{last+1},linear}$$            [13][$AUMC_{t_{last}-\infty,all}$]   (, 2013)  
                                                           the concentration-time curve                                                                                                                                                                                              
                                                          from $t_{last}$ to $\infty$ as                                                                                                                                                                                             
                                                              used for $AUC_{all}$.                                                                                                                                                                                                  

     $AUMC_{0-\infty,obs}$,       concentration*time^2^   Area under the first moment of         AUMCIFP, AUMCIFO           TRUE     FALSE        TRUE           TRUE                           $$AUMC_{last} +                          [14][$AUMC_{0-\infty,obs}$,       (, 2013)  
     $AUMC_{0-\infty,pred}$                                the concentration-time curve                                                                                                     AUMC_{t_{last}-\infty}$$                       $AUMC_{0-\infty,pred}$]                   
                                                            extrapolated to $\infty$,                                                                                                                                                                                                
                                                          calculated using the observed                                                                                                                                                                                              
                                                          or predicted value of the last                                                                                                                                                                                             
                                                             non-zero concentration.                                                                                                                                                                                                 

         $AUMC_{0,all}$           concentration*time^2^   Area under the first moment of                                    TRUE      TRUE        TRUE           TRUE                           $$AUMC_{last} +                              [15][$AUMC_{0,all}$]          (, 2013)  
                                                           the concentration-time curve                                                                                                   AUMC_{t_{last}-\infty,all}$$                                                               
                                                          from the time of dosing to the                                                                                                                                                                                             
                                                          time of the last observation,                                                                                                                                                                                              
                                                          regardless of whether the last                                                                                                                                                                                             
                                                          concentration is measurable or                                                                                                                                                                                             
                                                                       not.                                                                                                                                                                                                          

     $AUMC_{\%extrap,obs}$,                 %             Area under the first moment of         AUMCPEO, AUMCPEP           TRUE     FALSE        TRUE           TRUE           $$\frac{AUMC_{t_{last}-\infty}}{AUMC_{0,\infty}}         [16][$AUMC_{\%extrap,obs}$,       (, 2013)  
     $AUMC_{\%extrap,pred}$                                the concentration-time curve                                                                                                              \times                                $AUMC_{\%extrap,pred}$]                   
                                                              from the last observed                                                                                                                 100$$                                                                           
                                                           non-zero concentration value                                                                                                                                                                                              
                                                          to infinity as a percentage of                                                                                                                                                                                             
                                                             the area under the curve                                                                                                                                                                                                
                                                          extrapolated to infinity using                                                                                                                                                                                             
                                                              either the observed or                                                                                                                                                                                                 
                                                              predicted $C_{last}$.                                                                                                                                                                                                  

           $t_{1/2}$                      time                  Terminal half-life                    LAMZHL                TRUE      TRUE        TRUE           TRUE                      $$\frac{ln 2}{\lambda_z}$$                                                      (, 2013)  

          $\lambda_z$                    1/time           The first order rate constant                LAMZ                 TRUE      TRUE        TRUE           TRUE                      $$ln C = A - \lambda_z t$$                         [17][$\lambda_z$]            (, 2013)  
                                                           associated with the terminal                                                                                                                                                                                              
                                                           (log-linear) portion of the                                                                                                                                                                                               
                                                                      curve.                                                                                                                                                                                                         

     $t_{first,\lambda_z}$,               time            The first and last time (lower          LAMZLL, LAMZUL            TRUE      TRUE        TRUE           TRUE                                                                                                      (, 2013)  
      $t_{last,\lambda_z}$                                 and upper limit on time) for                                                                                                                                                                                              
                                                           values to be included in the                                                                                                                                                                                              
                                                           calculation of $\lambda_z$.                                                                                                                                                                                               

        $N_{\lambda_z}$                   count           The number of time points used              LAMZNPT               TRUE      TRUE        TRUE           TRUE                                                                       [18][$N_{\lambda_z}$]                    
                                                            in computing $\lambda_z$.                                                                                                                                                                                                

             $r^2$                      fraction          The goodness of fit statistic                 R2                  TRUE      TRUE        TRUE           TRUE                    $$1 - \frac{\sum_i \left(C_i -                          [19][$r^2$]                         
                                                           for the terminal elimination                                                                                                    \hat{C_i}\right)^2}{\sum_i                                                                
                                                                      phase.                                                                                                                      \left(C_i -                                                                        
                                                                                                                                                                                           \overline{C_i}\right)^2}$$                                                                

          $r^2_{adj}$                   fraction          The goodness of fit statistic                R2ADJ                TRUE      TRUE        TRUE           TRUE                      $$1 - \left(1 - r^2\right)                         [20][$r^2_{adj}$]            (, 2013)  
                                                           for the terminal elimination                                                                                                   \frac{1}{N_{\lambda_z}-2}$$                                                                
                                                          phase, adjusted for the number                                                                                                                                                                                             
                                                            of time points used in the                                                                                                                                                                                               
                                                            estimation of $\lambda_z$.                                                                                                                                                                                               

        $MRT_{ev,last}$,                  time            Mean residence time (MRT) from   MRTEVLST, MRTEVIFO, MRTEVIFP,    TRUE      TRUE        TRUE           TRUE                         $$\frac{AUMC}{AUC}$$                          [21][$MRT_{ev,last}$,          (, 2013)  
     $MRT_{ev,\infty,obs}$,                               the time of dosing to the time   MRTIVLST, MRTIVIFO, MRTIVIFP                                                                                                                     $MRT_{ev,\infty,obs}$,                   
    $MRT_{ev,\infty,pred}$,                                   of the last measurable                                                                                                                                                       $MRT_{ev,\infty,pred}$,                   
        $MRT_{iv,last}$,                                  concentration or infinity, for                                                                                                                                                       $MRT_{iv,last}$,                      
     $MRT_{iv,\infty,obs}$,                                a substance administered by                                                                                                                                                      $MRT_{iv,\infty,obs}$,                   
     $MRT_{iv,\infty,pred}$                               intravascular or extravascular                                                                                                                                                   $MRT_{iv,\infty,pred}$]                   
                                                                     dosing.                                                                                                                                                                                                         

         $MAT_{last}$,                    time              Mean absorption time of a                   MAT                 TRUE      TRUE        FALSE          TRUE                        $$MRT_{ev} - MRT{iv}$$                           [22][$MAT_{last}$,           (, 2013)  
      $MAT_{\infty,obs}$,                                   substance administered by                                                                                                     $$t_{lag} + \frac{1}{K_a}$$                        $MAT_{\infty,obs}$,                     
      $MAT_{\infty,pred}$                                     extravascular dosing.                                                                                                                                                          $MAT_{\infty,pred}$]                    

             $PTR$                        ratio             The maximum concentration                PTROUGHR              FALSE      TRUE        TRUE           TRUE                    $$\frac{C_{max}}{C_{trough}}$$                                                    (, 2013)  
                                                             during a dosing interval                                                                                                                                                                                                
                                                           divided by the concentration                                                                                                                                                                                              
                                                             at the end of the dosing                                                                                                                                                                                                
                                                                    interval.                                                                                                                                                                                                        

             $TPR$                        ratio           The concentration at the start             TROUGHPR              FALSE      TRUE        TRUE           TRUE                    $$\frac{C_{trough}}{C_{max}}$$                                                              
                                                           of a dosing interval divided                                                                                                                                                                                              
                                                           by the maximum concentration                                                                                                                                                                                              
                                                           during the dosing interval.                                                                                                                                                                                               

             $PTF$                          %              The difference between Cmin                 FLUCP               FALSE      TRUE        TRUE           TRUE                     $$100 \times \frac{C_{max} -                                                     (, 2013)  
                                                          and Cmax standardized to Cavg,                                                                                                      C_{min}}{C_{avg}}$$                                                                    
                                                          between dose time and $\tau$.                                                                                                                                                                                              

      $C_{avg}$, $C_{av}$             concentration           Average concentration                    CAVG                FALSE      TRUE        TRUE           TRUE                    $$\frac{AUC_{0,\tau}}{\tau}$$                                                     (, 2013)  

          $R_{A,AUC}$                   fraction           The area under the curve at                 ARAUC               FALSE      TRUE        TRUE           TRUE                            $$R_{A,AUC} =                                [23][$R_{A,AUC}$]            (, 2013)  
                                                           steady state divided by the                                                                                               \frac{AUC_{\tau,ss}}{AUC_{\tau,sd}}$$                                                           
                                                          area under the curve over the                                                                                                                                                                                              
                                                             initial dosing interval.                                                                                                                                                                                                

        $R_{A,C_{max}}$                 fraction           The maximum concentration at               ARCMAX               FALSE      TRUE        TRUE           TRUE                          $$R_{A,C_{max}} =                            [24][$R_{A,C_{max}}$]          (, 2013)  
                                                           steady state divided by the                                                                                                  \frac{C_{max,ss}}{C_{max,sd}}$$                                                              
                                                           maximum concentration during                                                                                                                                                                                              
                                                           the initial dosing interval.                                                                                                                                                                                              

        $R_{A,C_{min}}$                 fraction           The minimum concentration at               ARCMIN               FALSE      TRUE        TRUE           TRUE                          $$R_{A,C_{min}} =                            [25][$R_{A,C_{min}}$]          (, 2013)  
                                                           steady state divided by the                                                                                                  \frac{C_{min,ss}}{C_{min,sd}}$$                                                              
                                                           minimum concentration during                                                                                                                                                                                              
                                                           the initial dosing interval.                                                                                                                                                                                              

       $R_{A,C_{trough}}$               fraction           The trough concentration at               ARCTROUG              FALSE      TRUE        TRUE           TRUE                         $$R_{A,C_{trough}} =                         [26][$R_{A,C_{trough}}$]        (, 2013)  
                                                           steady state divided by the                                                                                               \frac{C_{trough,ss}}{C_{trough,sd}}$$                                                           
                                                           trough concentration during                                                                                                                                                                                               
                                                           the initial dosing interval.                                                                                                                                                                                              

 $CL_{ev,obs}$, $CL_{ev,pred}$,        volume/time         The total body clearance for    CLFO, CLFP, CLFTAU, CLO, CLP,    TRUE      TRUE        TRUE           TRUE                      $$\frac{F \times D}{AUC}$$                        [27][$CL_{ev,obs}$,           (, 2013)  
 $CL_{ev,\tau}$, $CL_{iv,obs}$,                           extravascular or intravascular               CLTAU                                                                                                                                   $CL_{ev,pred}$,                       
 $CL_{iv,pred}$, $CL_{iv,\tau}$                           administration (divided by the                                                                                                                                                $CL_{ev,\tau}$, $CL_{iv,obs}$,               
                                                          fraction of dose absorbed for                                                                                                                                                        $CL_{iv,pred}$,                       
                                                            extravascular), calculated                                                                                                                                                         $CL_{iv,\tau}$]                       
                                                           using the equivalent $AUC$.                                                                                                                                                                                               

  $V_{ss,obs}$, $V_{ss,pred}$            volume           The volume of distribution at             VSSO, VSSP              TRUE     FALSE        TRUE           FALSE                         $$CL \times MRT$$                              [28][$V_{ss,obs}$,           (, 2013)  
                                                            steady state based on the                                                                                                      $$\frac{F \times D \times                            $V_{ss,pred}$]                       
                                                            equivalent for a substance                                                                                                         AUMC}{{AUC}}^2}$$                                                                     
                                                          administered by intravascular                                                                                                                                                                                              
                                                                     dosing.                                                                                                                                                                                                         

        $V_{z,ev,obs}$,                  volume             The volume of distribution     VZFO, VZFP, VZFTAU, VZO, VZP,    TRUE      TRUE        TRUE           TRUE                    $$\frac{F \times D}{AUC \times                                                    (, 2013)  
        $V_{z,ev,pred}$,                                   associated with the terminal                VZTAU                                                                                      \lambda_z}$$                                                                       
        $V_{z,ev,\tau}$,                                  slope following extravascular                                                                                                                                                                                              
        $V_{z,iv,obs}$,                                          or intravascular                                                                                                                                                                                                    
        $V_{z,iv,pred}$,                                  administration (divided by the                                                                                                                                                                                             
        $V_{z,iv,\tau}$                                   fraction of dose absorbed for                                                                                                                                                                                              
                                                            extravascular), calculated                                                                                                                                                                                               
                                                             using equivalent $AUC$.                                                                                                                                                                                                 

             $C_0$                    concentration           Initial concentration                     C0                  TRUE      TRUE        TRUE           FALSE                                                                           [29][$C_0$]                         

             $V_0$                       volume               The initial volume of                     V0                  TRUE     FALSE        TRUE           FALSE                         $$\frac{D}{C_0}$$                                                           (, 2013)  
                                                           distribution for a substance                                                                                                                                                                                              
                                                              administered by bolus                                                                                                                                                                                                  
                                                              intravascular dosing.                                                                                                                                                                                                  

   $AUC_{\%backextrap,obs}$,       concentration*time                                                                       TRUE      TRUE        TRUE           FALSE              $$\frac{AUC_{0,first}}{AUC_{0,\infty}}$$            [30][$AUC_{\%backextrap,obs}$,               
   $AUC_{\%backextrap,pred}$                                                                                                                                                                                                              $AUC_{\%backextrap,pred}$]                 
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Notes

## $C_{min}$
Compare with $C_{trough}$.

## $C_{trough}$
Compare with $C_{min}$.

## $C_{last,pred}$
Parameters in the equation are fit during half-life fitting.

## $AUC_{0,t}$, $AUC_{last}$, $AUC_{\tau}$
Often, the $AUC_{a,b,linear}$ and $AUC_{a,b,log-linear}$ are combined where the linear trapezoidal rule is used for ascending concentrations ($C_{i+1} >= C_i$) or when the next concentration is below the limit of quantification ($C_{i+1} > 0$, if applicable), and the log-linear trapezoidal rule is used for descending concentrations $C_{i+1} < C_i$.

## $AUC_{t_{last}-\infty,pred}$, $AUC_{t_{last}-\infty,obs}$
$C_{last}$ should be $C_{last,pred}$ or $C_{last,obs}$ depending on which version of the parameter is desired.

## $AUC_{t_{last}-\infty,all}$
$t_{last+1}$ is the first time point below the limit of quantification.

## $AUC_{0-\infty,pred}$, $AUC_{0-\infty,obs}$
Use the 'pred' or 'obs' version of $AUC_{t_{last}-\infty}$ for the equivalent version of $AUC_{0-\infty}$.

## $AUC_{0,all}$
If all concentrations are above the limit of quantification, then $AUC_{0,all}=AUC_{last}$.

## $AUC_{\%extrap,obs}$, $AUC_{\%extrap,pred}$
Use the 'pred' or 'obs' version of $AUC_{t_{last},\infty}$ and $AUC_{0,\infty}$ for the equivalent version of $AUC_{\%extrap}$.

## $F$
Bioavailability is the ratio of two AUC values.  In addition to the comparison of extravascular ($ev$) to intravascular ($iv$) for absolute bioavailability, relative bioavailability compares any two $AUC_{0,\infty} values, a 'test' to a 'reference'$.  In some cases, bioavailability may be tested at steady-state using $AUC_{0,\tau}$ instead of $AUC_{0,\infty}$.

## $AUMC_{0,t}$, $AUMC_{last}$, $AUMC_{\tau}$
See $AUC_{last}$ notes for suggested calculation options.

## $AUMC_{t_{last}-\infty,obs}$, $AUMC_{t_{last}-\infty,pred}$
$C_{last}$ should be $C_{last,pred}$ or $C_{last,obs}$ depending on which version of the parameter is desired.

## $AUMC_{t_{last}-\infty,all}$
$t_{last+1}$ is the first time point below the limit of quantification.

## $AUMC_{0-\infty,obs}$, $AUMC_{0-\infty,pred}$
Use the 'obs' or 'pred' version of $AUC_{t_{last}-\infty}$ for the equivalent version of $AUC_{0-\infty}$.

## $AUMC_{0,all}$
If all concentrations are above the limit of quantification, then $AUMC_{0,all}=AUMC_{last}$.

## $AUMC_{\%extrap,obs}$, $AUMC_{\%extrap,pred}$
Use the 'pred' or 'obs' version of $AUMC_{t_{last}-\infty}$ for the equivalent version of $AUMC_{0-\infty}$.

## $\lambda_z$
Fit the equation using observed concentration ($C$) and time ($t$) from the terminal slope of the concentration-time curve.  Selection of points for inclusion may be either manual or regression-quality based.

## $N_{\lambda_z}$
$N_{\lambda_z}$ should always be greater than or equal to 3.

## $r^2$
$r^2$ is typically directly available from line-fitting functions and rarely requires direct calculation.  $\overline{C_i}$ is the mean concentration of values used; $\hat{C_i}$ is the estimated concentation.

## $r^2_{adj}$
The canonical form of $r^2_{adj}$ has the fraction on the right of the equation as $\frac{p}{n-p-1}$, but for fitting terminal regression $p=1$.

## $MRT_{ev,last}$, $MRT_{ev,\infty,obs}$, $MRT_{ev,\infty,pred}$, $MRT_{iv,last}$, $MRT_{iv,\infty,obs}$, $MRT_{iv,\infty,pred}$
The equation shown here includes the mean absorption time for extravascular administration aligning with the SDTM definition.  The $AUMC$ and $AUC$ should be chosen to match the parameter type desired (e.g. use $AUMC_{last}$ and $AUC_{last}$ for $MRT_{last}$).

## $MAT_{last}$, $MAT_{\infty,obs}$, $MAT_{\infty,pred}$
$K_a$ is the absorption rate from multi-exponential compartmental analysis curve fitting (and is not typically applicable for noncompartmental analysis).

## $R_{A,AUC}$
$ss$ indicates that value is at steady-state while $sd$ indicated that value is from the first (single) dose.

## $R_{A,C_{max}}$
$ss$ indicates that value is at steady-state while $sd$ indicated that value is from the first (single) dose.

## $R_{A,C_{min}}$
$ss$ indicates that value is at steady-state while $sd$ indicated that value is from the first (single) dose.

## $R_{A,C_{trough}}$
$ss$ indicates that value is at steady-state while $sd$ indicated that value is from the first (single) dose.

## $CL_{ev,obs}$, $CL_{ev,pred}$, $CL_{ev,\tau}$, $CL_{iv,obs}$, $CL_{iv,pred}$, $CL_{iv,\tau}$
For each of the symbols, select the equivalent $AUC$.  Such as, $CL_{ev,pred}$ uses $AUC = AUC_{0,\infty,pred}$

## $V_{ss,obs}$, $V_{ss,pred}$
SDTM parameters are specific to intravascular dosing.  For each of the symbols, select the equivalent $AUMC$ and $AUC$.  When extravascular dosing is used, it is referred to as the observed or apparent volume of distribution at steady-state.  CL and MRT may be given either for single dosing with $AUC_{0,\infty}$ or steady-state with $AUC_{0,\tau}$.

## $C_0$
IV bolus only.  $C_0$ is back-extrapolated from the first two data points after the infusion.  See data cleaning rules SDC-4 and MDC-4 for more details on the calculation and cleaning associated with $C_0$.

## $AUC_{\%backextrap,obs}$, $AUC_{\%backextrap,pred}$
IV bolus only.  $first$ is the first time point after 0, and both $AUC$ values should be calculated with $C_0$ included at time 0.

## References

[1] _Microsoft Word - PK-glossary\_ PK\_ working\_
group\_2004.doc_. <URL:
http://www.agah.eu/fileadmin/_migrated/content_uploads/PK-glossary_PK_working_group_2004.pdf>.
2013. <URL:
http://www.agah.eu/fileadmin/_migrated/content_uploads/PK-glossary_PK_working_group_2004.pdf>.


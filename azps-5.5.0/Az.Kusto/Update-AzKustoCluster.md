---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180420"
---
# Update-AzKustoCluster

## SYNOPSIS
Kusto 클러스터를 업데이트합니다.

## 구문

### UpdateExpanded(기본값)
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명
Kusto 클러스터를 업데이트합니다.

## 예제

### 예제 1: 이름에 의해 기존 클러스터 업데이트
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

위의 명령은 리소스 그룹 "testrg"에 있는 Kusto 클러스터 "testnewkustocluster"의 SKU를 업데이트합니다.

### 예제 2: 이름에 의해 기존 클러스터 업데이트
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

위의 명령은 리소스 그룹 "testrg"에 있는 클러스터 "testnewkustocluster"를 고객 관리 키로 업데이트합니다.

## PARAMETERS

### -AsJob
작업으로 명령 실행

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDiskEncryption
클러스터의 디스크가 암호화되어 있는 경우를 나타내는 부울 값입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDoubleEncryption
이중 암호화를 사용할 수 있는 경우를 나타내는 부울 값입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePurge
제거 작업이 사용 가능한지 나타내는 부울 값입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableStreamingIngest
스트리밍을 사용할 수 있는지 나타내는 부울 값입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EngineType
엔진 유형

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
사용되는 관리 ID의 유형입니다.
'SystemAssigned, UserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.
'없음' 형식은 모든 ID를 제거합니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityUserAssignedIdentity
Kusto 클러스터와 연결된 사용자 ID 목록입니다.
사용자 ID 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' 형식의 ARM 리소스 ID가 됩니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyVaultPropertyKeyName
키 자격 증명 모음 키의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultPropertyKeyVaultUri
키 자격 증명 모음의 URI입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultPropertyKeyVersion
키 자격 증명 모음 키의 버전입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultPropertyUserIdentity
키에 대한 액세스 권한이 ARM 사용자 할당 ID(리소스 ID)입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LanguageExtensionValue
언어 확장 목록입니다.
생성을 위해 LANGUAGEEXTENSIONVALUE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
리소스 위치입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Kusto 클러스터의 이름입니다.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
명령을 비동기적으로 실행

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OptimizedAutoscaleIsEnabled
최적화된 자동 조정 기능이 사용하도록 설정되어 있지 않은지 나타내는 부울 값입니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OptimizedAutoscaleMaximum
허용되는 최대 인스턴스 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OptimizedAutoscaleMinimum
허용되는 최소 인스턴스 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OptimizedAutoscaleVersion
정의된 템플릿의 버전입니다(예: 1).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuCapacity
클러스터의 인스턴스 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
SKU 이름입니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuTier
SKU 계층.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.
구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
리소스 태그.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustedExternalTenant
클러스터의 외부 테넌트입니다.
생성을 위해 TRUSTEDEXTERNALTENANT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkConfigurationDataManagementPublicIPId
데이터 관리의 서비스 공용 IP 주소 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkConfigurationEnginePublicIPId
엔진 서비스의 공용 IP 주소 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkConfigurationSubnetId
서브넷 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


INPUTOBJECT: <IKustoIdentity> ID 매개 변수
  - `[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.
  - `[ClusterName <String>]`: Kusto 클러스터의 이름입니다.
  - `[DataConnectionName <String>]`: 데이터 연결의 이름입니다.
  - `[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.
  - `[Id <String>]`: 리소스 ID 경로
  - `[Location <String>]`: Azure 위치입니다.
  - `[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.
  - `[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.
  - `[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다. 구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.

LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: 언어 확장 목록입니다.
  - `[Name <LanguageExtensionName?>]`: 언어 확장 이름입니다.

TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: 클러스터의 외부 테넌트입니다.
  - `[Value <String>]`: 외부 테넌트를 나타내는 GUID입니다.

## 관련 링크


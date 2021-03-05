---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: fbb45450352a99edc5a89d24ac8eb6bc4bcbf383
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987149"
---
# Update-AzVMWarePrivateCloud

## SYNOPSIS
사설 클라우드 업데이트

## 구문

### UpdateExpanded(기본값)
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명
사설 클라우드 업데이트

## 예제

### 예제 1: 이름에 따라 사설 클라우드의 크기 업데이트
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

이름에 따라 사설 클라우드의 업데이트 크기

### 예제 2: 입력 개체에 따라 사설 클라우드의 크기 업데이트
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

입력 개체에 따라 사설 클라우드의 크기 업데이트

## 매개 변수

### -AsJob
작업으로 명령을 실행합니다.

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
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -IdentitySource
vCenter Single Sign-On ID 원본을 생성하기 위해 IDENTITYSOURCE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Internet
인터넷에 대한 연결이 활성화되거나 비활성화되어 있습니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementClusterSize
클러스터 크기

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

### -Name
사설 클라우드의 이름

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
명령 비동기 실행

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

### -ResourceGroupName
리소스 그룹의 이름입니다.
이름은 대소문자와 무관합니다.

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

### -SubscriptionId
대상 구독의 ID입니다.

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
리소스 태그입니다.

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

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud

## 참고 사항

별칭

복잡한 매개 변수 속성

아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.


IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On ID 원본
  - `[Alias <String>]`: 도메인의 NetBIOS 이름
  - `[BaseGroupDn <String>]`: 그룹의 기본 구분 이름
  - `[BaseUserDn <String>]`: 사용자에 대한 기본 구분 이름
  - `[Domain <String>]`: 도메인의 dns 이름
  - `[Name <String>]`: ID 원본의 이름
  - `[Password <String>]`: 사용자 및 그룹에 대한 Base DN에 대한 읽기 전용 액세스가 최소인 Active Directory 사용자의 암호입니다.
  - `[PrimaryServer <String>]`: 기본 서버 URL
  - `[SecondaryServer <String>]`: 보조 서버 URL
  - `[Ssl <SslEnum?>]`: SSL 인증서(LDAPS)를 사용하여 LDAP 통신 보호
  - `[Username <String>]`: 사용자 및 그룹에 대한 Base DN에 대한 읽기 전용 액세스가 최소인 Active Directory 사용자의 ID

INPUTOBJECT <IVMWareIdentity> : ID 매개 변수
  - `[AuthorizationName <String>]`: 사설 클라우드의 ExpressRoute 회로 권한 부여 이름
  - `[ClusterName <String>]`: 사설 클라우드의 클러스터 이름
  - `[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise Site 이름
  - `[Id <String>]`: 리소스 ID 경로
  - `[Location <String>]`: Azure 지역
  - `[PrivateCloudName <String>]`: 사설 클라우드의 이름
  - `[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다. 이름은 대소문자와 무관합니다.
  - `[SubscriptionId <String>]`: 대상 구독의 ID입니다.

## 관련 링크


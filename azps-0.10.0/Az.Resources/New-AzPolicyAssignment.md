---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b8a7bd3d0c9f73b551cf6eefcb2564918fde1fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876435"
---
# New-AzPolicyAssignment

## SYNOPSIS
정책 할당을 만듭니다.

## 구문과

### DefaultParameterSet (기본값)
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### PolicyParameterObjectParameterSet
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicyParameterStringParameterSet
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicySetParameterObjectParameterSet
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicySetParameterStringParameterSet
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**새 AzPolicyAssignment** cmdlet은 정책 할당을 만듭니다.
정책 및 범위를 지정 합니다.

## 예제의

### 예제 1: 리소스 그룹 수준의 정책 할당
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져와 $ResourceGroup 변수에 저장 합니다.
두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 VirtualMachinePolicy 라는 정책 정의를 가져와 $Policy 변수에 저장 합니다.
마지막 명령은 $ResourceGroup의 **ResourceId** 속성으로 식별 되는 리소스 그룹의 수준에서 $Policy 정책을 할당 합니다.

### 예제 2: 정책 매개 변수 개체를 사용 하 여 리소스 그룹 수준의 정책 할당
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.
명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.
두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 허용 된 위치에 대 한 기본 제공 정책 정의를 가져옵니다.
명령이 $Policy 변수에 해당 개체를 저장 합니다.
세 번째와 네 번째 명령은 이름에 "동쪽"이 포함 된 모든 Azure 지역을 포함 하는 개체를 만듭니다.
명령은 $AllowedLocations 변수에 해당 개체를 저장 합니다.
마지막 명령은 $AllowedLocations의 정책 매개 변수 개체를 사용 하 여 리소스 그룹의 수준에서 $Policy 정책을 할당 합니다.
리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.

### 예제 3: 정책 매개 변수 파일이 있는 리소스 그룹 수준의 정책 할당
로컬 작업 디렉터리에 다음 콘텐츠를 포함 하는 _AllowedLocations.js_ 파일을 만듭니다.

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져와 $ResourceGroup 변수에 저장 합니다.
두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 허용 된 위치에 대 한 기본 제공 정책 정의를 가져와 $Policy 변수에 저장 합니다.
마지막 명령은 로컬 작업 디렉터리에서 정책 매개 변수 파일 AllowedLocations.js를 사용 하 여 $ResourceGroup의 **ResourceId** 속성으로 식별 되는 리소스 그룹의 $Policy 정책을 할당 합니다.

### 예제 4: 관리 id를 사용 하 여 정책 할당
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져와 $ResourceGroup 변수에 저장 합니다.
두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 VirtualMachinePolicy 라는 정책 정의를 가져와 $Policy 변수에 저장 합니다.
마지막 명령은 $Policy의 정책을 리소스 그룹에 할당 합니다. 관리 id가 자동으로 만들어지고 정책 할당에 할당 됩니다.

## 변수

### -ApiVersion
사용할 리소스 공급자 API의 버전을 지정 합니다.
버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.

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

### -Id 할당
이 정책 할당에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다. Id는 ' deployIfNotExists ' 정책에 대 한 배포를 실행 하는 경우에 사용 됩니다. Id를 할당할 때 위치가 필요 합니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -설명
정책 할당에 대 한 설명

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
정책 할당의 표시 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
정책 할당의 리소스 id 위치입니다. 이는-할당 Id 스위치를 사용 하는 경우에 필요 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Metadata
새 정책 할당에 대 한 메타 데이터입니다. 메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 문자열로 지정할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
정책 할당의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotScope
정책 할당의 범위를 지정 하지 않습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinition
정책을 정책 규칙을 포함 하는 **PsPolicyDefinition** 개체로 지정 합니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameter
정책 매개 변수 파일 경로 또는 정책 매개 변수 문자열입니다.

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameterObject
정책 매개 변수 개체입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicySetDefinition
정책 집합 정의 개체입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.

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

### -범위
정책을 할당할 범위를 지정 합니다.
예를 들어 리소스 그룹에 정책을 할당 하려면 다음을 지정 합니다. `/subscriptions/` 구독 ID `/resourcegroups/` 리소스 그룹 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
SKU 속성을 나타내는 해시 테이블입니다. 기본적으로 다음 값이 포함 된 무료 SKU로 설정 `@{Name = 'A0'; Tier = 'Free'}` 됩니다. 표준 SKU를 사용 하려면 다음 값을 사용 합니다 `@{Name = 'A1'; Tier = 'Standard'}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzPolicyDefinition](./Get-AzPolicyDefinition.md)

[Get-AzPolicyAssignment](./Get-AzPolicyAssignment.md)

[제거-AzPolicyAssignment](./Remove-AzPolicyAssignment.md)

[Set-AzPolicyAssignment](./Set-AzPolicyAssignment.md)



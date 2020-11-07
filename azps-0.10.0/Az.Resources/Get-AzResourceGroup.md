---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: d09031270e61be80228003ae2a9ae47a5ce5ac74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876471"
---
# Get-AzResourceGroup

## SYNOPSIS
리소스 그룹을 가져옵니다.

## 구문과

### GetByResourceGroupName (기본값)
```
Get-AzResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹을 가져옵니다.
모든 리소스 그룹을 가져오거나 이름 또는 다른 속성을 기준으로 리소스 그룹을 지정할 수 있습니다.
기본적으로이 cmdlet은 현재 구독의 모든 리소스 그룹을 가져옵니다.
Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzResourceGroup cmdlet을 참조 하세요.

## 예제의

### 예제 1: 이름별로 리소스 그룹 가져오기
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

이 명령은 EngineerBlog 이라는 구독에서 Azure 리소스 그룹을 가져옵니다.

### 예제 2: 리소스 그룹의 모든 태그 가져오기
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

이 명령은 ContosoRG 이라는 리소스 그룹을 가져오고 해당 그룹과 연결 된 태그를 표시 합니다.

### 예제 3: 위치를 기준으로 리소스 그룹 표시
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### 예제 4: 특정 위치에 있는 모든 리소스 그룹의 이름 표시
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### 예제 5: 이름이 WebServer로 시작 하는 리소스 그룹 표시
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

## 변수

### -ApiVersion
리소스 공급자가 지 원하는 API 버전을 지정 합니다.
기본 버전 외의 다른 버전을 지정할 수 있습니다.

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

### -Id
가져올 리소스 그룹의 ID를 지정 합니다.
와일드 카드 문자는 허용 되지 않습니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
가져올 리소스 그룹의 위치를 지정 합니다.

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
가져올 리소스 그룹의 이름을 지정 합니다. 이 매개 변수는 문자열의 시작 및/또는 끝에 있는 와일드 카드를 지원 합니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
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

### 태그
리소스 그룹을 필터링 하는 태그 해시 테이블입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### ResourceManagement PSResourceGroup.

## 상속자

## 관련 링크

[새로운 AzResourceGroup](./New-AzResourceGroup.md)

[제거-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)



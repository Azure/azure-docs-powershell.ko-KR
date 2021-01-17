---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490503"
---
# Get-AzResourceGroup

## SYNOPSIS
리소스 그룹을 얻습니다.

## 구문

### GetByResourceGroupName(기본값)
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹을 얻습니다.
모든 리소스 그룹을 얻거나 이름 또는 다른 속성으로 리소스 그룹을 지정할 수 있습니다.
기본적으로 이 cmdlet은 현재 구독의 모든 리소스 그룹을 얻습니다.
Azure 리소스 및 Azure 리소스 그룹에 대한 자세한 내용은 New-AzResourceGroup 참조하세요.

## 예제

### 예제 1: 이름으로 리소스 그룹 얻기
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

이 명령은 EngineerBlog라는 구독에서 Azure 리소스 그룹을 얻습니다.

### 예제 2: 리소스 그룹의 모든 태그를 얻습니다.
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

이 명령은 ContosoRG라는 리소스 그룹을 얻게 하여 해당 그룹과 연결된 태그를 표시합니다.

### 예제 3: 태그를 기반으로 리소스 그룹 얻기
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### 예제 4: 위치로 리소스 그룹 표시
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### 예제 5: 특정 위치에 있는 모든 리소스 그룹의 이름 표시
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### 예제 6: 이름이 WebServer로 시작하는 리소스 그룹 표시
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## PARAMETERS

### -ApiVersion
리소스 공급자가 지원하는 API 버전을 지정합니다.
기본 버전과 다른 버전을 지정할 수 있습니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
얻을 리소스 그룹의 ID를 지정합니다.
와일드카드 문자는 허용되지 않습니다.

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

### -Location
얻을 리소스 그룹의 위치를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
얻을 리소스 그룹의 이름을 지정합니다. 이 매개 변수는 문자열의 시작 및/또는 끝에 와일드카드를 지원합니다.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -Pre
이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.

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

### -Tag
리소스 그룹을 필터링할 태그 해시테이블입니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Collections.Hashtable

## 출력

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## 참고 사항

## 관련 링크

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)


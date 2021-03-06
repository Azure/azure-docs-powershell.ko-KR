---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 2282bdef70f6352caa535b4d7a68d5e4046f831e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524936"
---
# Set-AzureRmRoleDefinition

## SYNOPSIS
Azure RBAC의 사용자 지정 역할을 수정 합니다.
수정 된 역할 정의를 JSON 파일 또는 PSRoleDefinition으로 제공 합니다.
먼저 Get-AzureRmRoleDefinition 명령을 사용 하 여 수정할 사용자 지정 역할을 검색 합니다.
그런 다음 변경할 속성을 수정 합니다.
마지막으로,이 명령을 사용 하 여 역할 정의를 저장 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### InputFileParameterSet
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Set-AzureRmRoleDefinition cmdlet은 Azure Role-Based Access Control의 기존 사용자 지정 역할을 업데이트 합니다.
업데이트 된 역할 정의를 JSON 파일 또는 PSRoleDefinition 개체로 명령에 대 한 입력으로 제공 합니다.
업데이트 된 사용자 지정 역할에 대 한 역할 정의에는 이름, 설명, 동작, AssignableScopes 업데이트 되지 않은 경우에도 해당 역할의 Id 및 기타 모든 필수 속성이 포함 되어야 합니다.
NotActions, DataActions, NotDataActions는 선택 사항입니다.

다음은 Set-AzureRmRoleDefinition에 대 한 업데이트 된 역할 정의 json 예제입니다.

{"Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "이름": "업데이트 된 역할", "설명": "모든 리소스를 모니터링 하 고 가상 컴퓨터를 시작 하 고 다시 시작할 수 있습니다.", "작업": \[ " */read", "ClassicCompute/virtualmachines/다시 시작/동작", "Microsoft. ClassicCompute/virtualmachines/start/action" \] , "notactions": \[ "* /Cwrite" \] , "dataactions": " \[ Microsoft 저장소/storageaccounts/blobservices/컨테이너/blob/read" \] , "Notdataaction": \[ "Microsoft. 저장소/storageaccounts/blobservices/컨테이너/blob/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## 예제의

### PSRoleDefinitionObject를 사용 하 여 업데이트
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### JSON 파일을 사용 하 여 만들기
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
업데이트 될 단일 json 역할 정의가 포함 된 파일 이름입니다.
JSON에서 업데이트 되는 속성만 포함 합니다.
Id 속성이 필요 합니다.

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -역할
업데이트할 역할 정의 개체

```yaml
Type: PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSRoleDefinition
' Role ' 매개 변수는 파이프라인에서 ' PSRoleDefinition ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. a. PSRoleDefinition (.Resources.

## 상속자
키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포

## 관련 링크

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[새로운 AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[제거-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)


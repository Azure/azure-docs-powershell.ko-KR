---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 47b519b324018e4fc369d281f7fb7eac554ac571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034589"
---
# Remove-AzKustoDatabase

## SYNOPSIS
기존 Kusto 데이터베이스를 삭제 합니다.

## 구문과

### ByNameAndResourceGroup (기본값)
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
기존 Kusto 데이터베이스를 삭제 합니다.

## 예제의

### 예제 1-이름으로 기존 Kusto 데이터베이스를 삭제 합니다.

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

위의 명령은 리소스 그룹 "testrg"에 있는 "mykustocluster" 클러스터에서 "mykustodatabase" 이라는 이름으로 Kusto 데이터베이스를 삭제 합니다.

### 예제 2-파이핑을 통해 기존 Kusto 데이터베이스를 삭제 합니다.

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

위 명령에서는 cmdlet을 사용 하 여 리소스 그룹 "testrg"에 있는 "mykustocluster" 클러스터에서 "mykustodatabase" 이라는 이름의 "이름" 데이터베이스를 가져온 `Get-AzKustoDatabase` 다음 결과를 `Remove-AzKustoDatabase` 삭제 하도록 검색 합니다.

## 변수

### -ClusterName
데이터베이스가 있는 클러스터의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -InputObject
데이터베이스 개체에는 kusto가 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
제거할 데이터베이스의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
지정 된 데이터베이스가 성공적으로 일시 중단 되었는지 여부를 반환 합니다.

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
클러스터가 있는 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
데이터베이스 ResourceID에 대 한 kusto

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### PSKustoDatabase를 위한 명령입니다.

## 출력

### 시스템 부울

## 상속자

## 관련 링크

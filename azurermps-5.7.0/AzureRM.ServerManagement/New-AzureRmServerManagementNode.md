---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: 498be36141d1a44d33cdcb351b92d5b6908071c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524924"
---
# New-AzureRmServerManagementNode

## SYNOPSIS
서버 관리 노드를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByName
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmServerManagementNode** Cmdlet은 Azure 서버 관리 노드를 만듭니다.

## 예제의

## 변수

### -ComputerName
관리 되는 컴퓨터의 컴퓨터 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
서버 관리 노드에 대 한 연결에 대 한 **PSCredential** 개체를 지정 합니다.
자격 증명 개체를 가져오려면 Get-Credential cmdlet을 사용 합니다.
자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -게이트웨이
노드를 관리 하는 게이트웨이를 지정 합니다.

이 매개 변수는 *ResourceGroupName* , *게이트웨이 이름* 및 *위치* 매개 변수 대신 사용할 수 있습니다.

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### --게이트웨이 이름
노드에 액세스 하는 게이트웨이의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
이 cmdlet이 노드를 만드는 위치를 지정 합니다.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeName
노드의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 노드를 만드는 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
개체와 연결 된 키/값 쌍입니다.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 게이트웨이와
' Gateway ' 매개 변수는 파이프라인에서 ' Gateway ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. ServerManagement. 모델 노드

## 상속자

## 관련 링크

[Get-AzureRmServerManagementNode](./Get-AzureRmServerManagementNode.md)

[제거-AzureRmServerManagementNode](./Remove-AzureRmServerManagementNode.md)



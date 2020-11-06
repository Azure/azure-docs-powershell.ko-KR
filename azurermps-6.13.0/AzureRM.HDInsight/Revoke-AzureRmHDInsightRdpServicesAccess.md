---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 8c3fd2340c1e15d5229a5fdfe9331b1d31c8c02a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535923"
---
# Revoke-AzureRmHDInsightRdpServicesAccess

## SYNOPSIS
Windows 클러스터에 대 한 RDP 액세스를 사용 하지 않도록 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmHDInsightRdpServicesAccess** Cmdlet은 Windows 기반 Azure HDInsight 클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스를 사용 하지 않도록 설정 합니다.

## 예제의

### 예제 1: 지정 된 클러스터에 대 한 RDP 액세스 사용 안 함
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

이 명령은-hadoop-001 이라는 클러스터에 대 한 RDP 액세스를 해지 합니다.

## 변수

### -ClusterName
클러스터의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### 시스템. i a o

## 상속자

## 관련 링크

[부여-AzureRmHDInsightRdpServicesAccess](./Grant-AzureRmHDInsightRdpServicesAccess.md)



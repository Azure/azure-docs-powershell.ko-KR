---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 304d64e2eaff4ae1488bdde12991d22834022e93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537775"
---
# New-AzureBatchCertificate

## SYNOPSIS
지정 된 Batch 계정에 인증서를 추가 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 파일 (기본값)
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RawData
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**새-AzureBatchCertificate** cmdlet은 지정 된 Azure Batch 계정에 인증서를 추가 합니다.

## 예제의

### 예제 1: 파일에서 인증서 추가
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

이 명령은 E:\Certificates\MyCert.cer. 파일을 사용 하 여 지정 된 Batch 계정에 인증서를 추가 합니다.

### 예제 2: 원시 데이터의 인증서 추가
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

첫 번째 명령은 MyCert 이라는 파일의 데이터를 $RawData 변수로 읽습니다.

두 번째 명령은 $RawData에 저장 된 원시 데이터를 사용 하 여 지정 된 Batch 계정에 인증서를 추가 합니다.

## 변수

### -BatchContext
이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.
Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다. 대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다. 공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다. 사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -FilePath
인증서 파일의 경로를 지정 합니다.
인증서 파일은 .cer 또는 .pfx 형식 중 하나 여야 합니다.

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -암호
인증서 개인 키에 액세스 하는 데 사용할 암호를 지정 합니다.
.Pfx 형식의 인증서를 지정 하는 경우이 매개 변수를 지정 해야 합니다.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RawData
.Cer 또는 .pfx 형식의 원시 인증서 데이터를 지정 합니다.

```yaml
Type: Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### BatchAccountContext
' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.

### Byte []
' RawData ' 매개 변수는 파이프라인에서 ' Byte [] ' 형식의 값을 허용 합니다.

## 출력

## 상속자

## 관련 링크

[Get-AzureBatchCertificate](./Get-AzureBatchCertificate.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[-AzureBatchCertificate 제거](./Remove-AzureBatchCertificate.md)

[Azure Batch Cmdlet](./AzureRM.Batch.md)



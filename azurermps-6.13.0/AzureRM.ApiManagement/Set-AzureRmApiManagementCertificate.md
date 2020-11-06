---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7712a7938617d979dad2feabf4d2b2126e20433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524683"
---
# Set-AzureRmApiManagementCertificate

## SYNOPSIS
백엔드를 사용 하 여 상호 인증 하도록 구성 된 API Management 인증서를 수정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### LoadFromFile (기본값)
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 순수
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmApiManagementCertificate** Cmdlet은 Azure API Management 인증서를 수정 합니다.

## 예제의

### 예제 1: 인증서 수정
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

이 명령은 지정 된 API Management 인증서를 수정 합니다.

## 변수

### -CertificateId
수정할 인증서의 ID를 지정 합니다.

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

### -컨텍스트
**PsApiManagementContext** 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -PassThru
passthru

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxBytes
.Pfx 형식의 인증서 파일 바이트 배열을 지정 합니다.
*PfxFilePath* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxFilePath
.Pfx 형식의 인증서 파일에 대 한 경로를 만들고 업로드할 지정 합니다.
*PfxBytes* 매개 변수를 지정 하지 않으면이 매개 변수가 필요 합니다.

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxPassword
인증서에 대 한 암호를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### ApiManagement. ServiceManagement. \ PsApiManagementContext

### System. 문자열

### Byte []

### System.webserver 매개 변수

## 출력

### ApiManagement. ServiceManagement. \ PsApiManagementCertificate

## 상속자

## 관련 링크

[Get-AzureRmApiManagementCertificate](./Get-AzureRmApiManagementCertificate.md)

[새로운 AzureRmApiManagementCertificate](./New-AzureRmApiManagementCertificate.md)

[제거-AzureRmApiManagementCertificate](./Remove-AzureRmApiManagementCertificate.md)



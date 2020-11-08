---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216591"
---
# New-AzWebAppAzureStoragePath

## SYNOPSIS
웹 앱에 탑재할 Azure 저장소 경로를 나타내는 개체를 만듭니다. 이 매개 변수는 Set-AzWebApp (-AzureStoragePath)로 사용 하기 위한 것입니다 Set-AzWebAppSlot

## 구문과

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
웹 앱 내에 탑재할 Azure 저장소 경로를 나타내는 개체를 만듭니다.

## 예제의

### 예제 1
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## 변수

### -AccessKey
Azure 저장소 계정에 대 한 선택 키

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountName
Azure 저장소 계정 이름입니다.
예: myfilestorageaccount.file.core.windows.net

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MountPath
ShareName에 의해 지정 된 공유가 노출 되는 컨테이너의 경로

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
Azure Storage 속성의 식별자입니다.
웹 앱 또는 슬롯 내에서 고유 해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareName
컨테이너에 탑재할 공유의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Azure 저장소 계정의 유형입니다.
Windows 컨테이너는 Azure 파일만 지원 합니다.

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

### 않아야

## 출력

### WebAppAzureStoragePath를 다운로드 하세요.

## 상속자

## 관련 링크

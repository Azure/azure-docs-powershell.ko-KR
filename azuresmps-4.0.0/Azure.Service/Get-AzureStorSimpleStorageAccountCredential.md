---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045551"
---
# Get-AzureStorSimpleStorageAccountCredential

## SYNOPSIS
저장소 계정에 대 한 자격 증명을 가져옵니다.

## 구문과

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**Get-AzureStorSimpleStorageAccountCredential** cmdlet은 저장소 계정에 대 한 자격 증명을 가져옵니다.
이 cmdlet은 서비스 또는 명명 된 **Storageaccountcredential** 에 구성 된 모든 **storageaccountcredential** 개체를 가져옵니다.

## 예제의

### 예제 1: 리소스에 대 한 모든 자격 증명 가져오기
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

이 명령은 현재 리소스의 저장소 계정에 대해 사용 가능한 자격 증명을 모두 가져옵니다.

### 예제 2: 특정 저장소 계정에 대 한 자격 증명 가져오기
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

이 명령은 ContosoCloudStorage 이라는 저장소 계정에 대 한 저장소 계정 자격 증명을 가져옵니다.

## 변수

### -프로필
Azure 프로필을 지정 합니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
자격 증명을 가져올 저장소 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### StorageAccountCredential, IList\<StorageAccountCredential\>
Storageaccountname 매개 변수를 지정 하거나 해당 매개 변수를 지정 하지 *StorageAccountName* 않은 경우이 Cmdlet은 **storageaccountcredential** 개체를 반환 하 고 **\<StorageAccountCredential\> IList** 개체를 반환 합니다.

## 상속자

## 관련 링크

[새-AzureStorSimpleStorageAccountCredential](./New-AzureStorSimpleStorageAccountCredential.md)

[-AzureStorSimpleStorageAccountCredential 제거](./Remove-AzureStorSimpleStorageAccountCredential.md)

[Set-AzureStorSimpleStorageAccountCredential](./Set-AzureStorSimpleStorageAccountCredential.md)



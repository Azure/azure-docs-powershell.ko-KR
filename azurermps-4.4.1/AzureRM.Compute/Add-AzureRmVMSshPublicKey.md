---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: 24c97e73728dab656a1d9fe3283e4eba6aae4ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525708"
---
# Add-AzureRmVMSshPublicKey

## SYNOPSIS
가상 컴퓨터에 대 한 SSH 공개 키를 추가 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmVMSshPublicKey** Cmdlet은 보안 셸 (SSH)을 통해 가상 컴퓨터에 연결 하는 데 사용할 수 있는 공개 키를 추가 합니다.

## 예제의

### 예제 1: 가상 컴퓨터에 공개 키 추가
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

첫 번째 명령은 **AzureRmVM** cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.
명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.

두 번째 명령은 Path 매개 변수에서 지정 하는 VirtualMachine07의 위치에 공개 키를 추가 합니다.

## 변수

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

### -KeyData
공개 키의 기본 64 인코딩을 지정 합니다.
SSH를 사용 하거나이 매개 변수에서 지정 하는 키를 사용 하 여 가상 컴퓨터에 연결할 수 있습니다.

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

### -Path
가상 머신에서이 cmdlet이 SSH 공개 키를 저장 하는 파일의 전체 경로를 지정 합니다.
파일이 이미 있는 경우이 cmdlet은 파일에 키를 추가 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 [AzureRmVM](./Get-AzureRmVM.md) cmdlet을 사용 합니다.
[새 AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureRmVM](./Get-AzureRmVM.md)

[새로운 AzureRmVMConfig](./New-AzureRmVMConfig.md)

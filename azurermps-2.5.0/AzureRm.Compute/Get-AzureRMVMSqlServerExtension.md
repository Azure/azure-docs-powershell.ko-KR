---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 6b02a83c7664fa460cd4ebd25a1754a8bc57e784
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883177"
---
# Get-AzureRmVMSqlServerExtension

## SYNOPSIS
가상 컴퓨터의 SQL Server 확장에 대 한 설정을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmVMSqlServerExtension** cmdlet은 가상 컴퓨터의 IAAS (SQL Server 인프라 as Services) 에이전트 설정을 가져옵니다.

## 예제의

### 예제 1: 가상 컴퓨터에서 SQL Server 확장의 설정 가져오기
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

이 명령은 ContosoVM07 이라는 가상 컴퓨터에서 SQL Server 확장의 설정을 가져옵니다.

### 예제 2: 파이프라인을 사용 하 여 설정 가져오기
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

이 명령은 Get-AzureRmVM cmdlet을 사용 하 여 서비스 Service08에서 ContosoVM22 라는 가상 컴퓨터를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 결과를 현재 cmdlet에 전달 합니다.

현재 명령은 해당 가상 컴퓨터에서 SQL Server IaaS 에이전트의 설정을 가져옵니다.

### 예제 3: 특정 SQL Server 버전의 설정 가져오기
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

이 명령은 ContosoVM07 이라는 가상 컴퓨터에서 SQL Server 확장의 버전 1.0에 대 한 설정을 가져옵니다.

## 변수

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

### -이름
확장 하는 SQL Server의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
가상 컴퓨터의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### VirtualMachineSqlServerExtensionContext를 계산 합니다.

## 상속자

## 관련 링크

[Get-AzureRmVM](./Get-AzureRmVM.md)

[제거-AzureRmVMSqlServerExtension](./Remove-AzureRMVMSqlServerExtension.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)



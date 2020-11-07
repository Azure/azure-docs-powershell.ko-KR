---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 97eae8c5c545297a7d6287a951ec02433d591168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879361"
---
# <span data-ttu-id="ebff1-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="ebff1-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="ebff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebff1-102">SYNOPSIS</span></span>
<span data-ttu-id="ebff1-103">보호 가능한 항목에 대 한 자동 백업을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="ebff1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebff1-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebff1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ebff1-105">DESCRIPTION</span></span>
<span data-ttu-id="ebff1-106">**AzRecoveryServicesBackupAutoProtection** cmdlet은 보호 가능한 항목에 대 한 보호가 사용 되지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="ebff1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ebff1-107">EXAMPLES</span></span>

### <span data-ttu-id="ebff1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ebff1-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="ebff1-109">첫 번째 cmdlet은 백업 보호 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="ebff1-110">변수</span><span class="sxs-lookup"><span data-stu-id="ebff1-110">PARAMETERS</span></span>

### <span data-ttu-id="ebff1-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ebff1-111">-BackupManagementType</span></span>
<span data-ttu-id="ebff1-112">리소스의 백업 관리 유형 (예: MAB, DPM)입니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebff1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebff1-113">-DefaultProfile</span></span>
<span data-ttu-id="ebff1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebff1-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="ebff1-115">-InputItem</span></span>
<span data-ttu-id="ebff1-116">항목 Id</span><span class="sxs-lookup"><span data-stu-id="ebff1-116">Item Id</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebff1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebff1-117">-PassThru</span></span>
<span data-ttu-id="ebff1-118">자동 보호에 대 한 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-118">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="ebff1-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ebff1-119">-VaultId</span></span>
<span data-ttu-id="ebff1-120">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebff1-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ebff1-121">-WorkloadType</span></span>
<span data-ttu-id="ebff1-122">리소스의 작업 부하 유형 (예: Add-azurevm, WindowsServer, AzureFiles)</span><span class="sxs-lookup"><span data-stu-id="ebff1-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebff1-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ebff1-123">-Confirm</span></span>
<span data-ttu-id="ebff1-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebff1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebff1-125">-WhatIf</span></span>
<span data-ttu-id="ebff1-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebff1-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebff1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebff1-128">CommonParameters</span></span>
<span data-ttu-id="ebff1-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebff1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebff1-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebff1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebff1-131">입력</span><span class="sxs-lookup"><span data-stu-id="ebff1-131">INPUTS</span></span>

### <span data-ttu-id="ebff1-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ebff1-132">System.String</span></span>

## <span data-ttu-id="ebff1-133">출력</span><span class="sxs-lookup"><span data-stu-id="ebff1-133">OUTPUTS</span></span>

### <span data-ttu-id="ebff1-134">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ebff1-134">System.Boolean</span></span>

## <span data-ttu-id="ebff1-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ebff1-135">NOTES</span></span>

## <span data-ttu-id="ebff1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebff1-136">RELATED LINKS</span></span>

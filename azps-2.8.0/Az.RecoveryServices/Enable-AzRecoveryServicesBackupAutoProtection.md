---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: a17c7b8addf1bf1218131e8e950185d9da6c22d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872794"
---
# <span data-ttu-id="48fb9-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="48fb9-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="48fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="48fb9-103">이 명령을 사용 하면 사용자가 기존에 보호 되지 않은 모든 DB 및 나중에 지정 된 정책에 추가 되는 모든 데이터베이스를 자동으로 보호할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="48fb9-104">Azure backup service는 새 Db에 대해 자동 보호 컨테이너를 정기적으로 검사 하 여 자동으로 보호 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="48fb9-105">구문과</span><span class="sxs-lookup"><span data-stu-id="48fb9-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48fb9-106">설명은</span><span class="sxs-lookup"><span data-stu-id="48fb9-106">DESCRIPTION</span></span>
<span data-ttu-id="48fb9-107">**AzRecoveryServicesBackupAutoProtection** cmdlet은 보호 가능한 항목에 대 한 Azure 자동 백업 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="48fb9-108">예제의</span><span class="sxs-lookup"><span data-stu-id="48fb9-108">EXAMPLES</span></span>

### <span data-ttu-id="48fb9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="48fb9-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="48fb9-110">첫 번째 cmdlet은 기본 정책 개체를 가져온 다음 $Pol 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="48fb9-111">두 번째 cmdlet은 $Pol의 정책을 사용 하 여 AzureWorkload 부하에 대 한 백업 보호 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="48fb9-112">변수</span><span class="sxs-lookup"><span data-stu-id="48fb9-112">PARAMETERS</span></span>

### <span data-ttu-id="48fb9-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="48fb9-113">-BackupManagementType</span></span>
<span data-ttu-id="48fb9-114">리소스의 백업 관리 유형 (예: MAB, DPM, AzureWorkload)입니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

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

### <span data-ttu-id="48fb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48fb9-115">-DefaultProfile</span></span>
<span data-ttu-id="48fb9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48fb9-117">-InputItem</span><span class="sxs-lookup"><span data-stu-id="48fb9-117">-InputItem</span></span>
<span data-ttu-id="48fb9-118">입력으로 전달할 수 있는 보호 가능한 항목 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-118">Specifies the protectable item object that can be passed as an input.</span></span>

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

### <span data-ttu-id="48fb9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48fb9-119">-PassThru</span></span>
<span data-ttu-id="48fb9-120">자동 보호에 대 한 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-120">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="48fb9-121">-정책</span><span class="sxs-lookup"><span data-stu-id="48fb9-121">-Policy</span></span>
<span data-ttu-id="48fb9-122">보호 정책 개체.</span><span class="sxs-lookup"><span data-stu-id="48fb9-122">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48fb9-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="48fb9-123">-VaultId</span></span>
<span data-ttu-id="48fb9-124">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="48fb9-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="48fb9-125">-WorkloadType</span></span>
<span data-ttu-id="48fb9-126">리소스의 작업 부하 유형 (예: Add-azurevm, WindowsServer, AzureFiles, MSSQL)입니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="48fb9-127">-확인</span><span class="sxs-lookup"><span data-stu-id="48fb9-127">-Confirm</span></span>
<span data-ttu-id="48fb9-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48fb9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48fb9-129">-WhatIf</span></span>
<span data-ttu-id="48fb9-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48fb9-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48fb9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48fb9-132">CommonParameters</span></span>
<span data-ttu-id="48fb9-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48fb9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48fb9-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48fb9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48fb9-135">입력</span><span class="sxs-lookup"><span data-stu-id="48fb9-135">INPUTS</span></span>

### <span data-ttu-id="48fb9-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="48fb9-136">System.String</span></span>

## <span data-ttu-id="48fb9-137">출력</span><span class="sxs-lookup"><span data-stu-id="48fb9-137">OUTPUTS</span></span>

### <span data-ttu-id="48fb9-138">System. 개체</span><span class="sxs-lookup"><span data-stu-id="48fb9-138">System.Object</span></span>

## <span data-ttu-id="48fb9-139">상속자</span><span class="sxs-lookup"><span data-stu-id="48fb9-139">NOTES</span></span>

## <span data-ttu-id="48fb9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48fb9-140">RELATED LINKS</span></span>
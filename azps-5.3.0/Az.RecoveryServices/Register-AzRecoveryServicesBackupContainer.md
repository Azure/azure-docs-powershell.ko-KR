---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492435"
---
# <span data-ttu-id="1204d-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1204d-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="1204d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1204d-102">SYNOPSIS</span></span>
<span data-ttu-id="1204d-103">**Register-AzRecoveryServicesBackupContainer** cmdlet은 특정 workloadType을 사용하여 AzureWorkloads용 Azure VM을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="1204d-104">구문</span><span class="sxs-lookup"><span data-stu-id="1204d-104">SYNTAX</span></span>

### <span data-ttu-id="1204d-105">등록(기본값)</span><span class="sxs-lookup"><span data-stu-id="1204d-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1204d-106">ReRegister</span><span class="sxs-lookup"><span data-stu-id="1204d-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1204d-107">설명</span><span class="sxs-lookup"><span data-stu-id="1204d-107">DESCRIPTION</span></span>
<span data-ttu-id="1204d-108">이 명령을 사용하면 Azure Backup에서 리소스를 백업 컨테이너로 변환한 다음, 해당 Recovery Services 자격 증명 모음에 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="1204d-109">Azure Backup 서비스는 나중에 보호할 이 컨테이너 내에서 주어진 워크로드 유형의 워크로드를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="1204d-110">예제</span><span class="sxs-lookup"><span data-stu-id="1204d-110">EXAMPLES</span></span>

### <span data-ttu-id="1204d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1204d-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="1204d-112">cmdlet은 Azure VM을 워크로드 MSSQL에 대한 컨테이너로 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="1204d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1204d-113">PARAMETERS</span></span>

### <span data-ttu-id="1204d-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1204d-114">-BackupManagementType</span></span>
<span data-ttu-id="1204d-115">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-115">The class of resources being protected.</span></span> <span data-ttu-id="1204d-116">현재 이 cmdlet에 지원되는 값은 AzureWorkload입니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1204d-117">-Container</span><span class="sxs-lookup"><span data-stu-id="1204d-117">-Container</span></span>
<span data-ttu-id="1204d-118">항목이 있는 컨테이너</span><span class="sxs-lookup"><span data-stu-id="1204d-118">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1204d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1204d-119">-DefaultProfile</span></span>
<span data-ttu-id="1204d-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1204d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1204d-121">-Force</span></span>
<span data-ttu-id="1204d-122">컨테이너를 강제로 등록합니다(확인 대화 상자 방지).</span><span class="sxs-lookup"><span data-stu-id="1204d-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="1204d-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="1204d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1204d-124">-ResourceId</span></span>
<span data-ttu-id="1204d-125">구독의 일부 RecoveryServices 자격 증명 모음에 의해 이미 보호되어 있는 경우 대표 항목을 검사해야 하는 Azure 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1204d-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1204d-126">-VaultId</span></span>
<span data-ttu-id="1204d-127">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1204d-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1204d-128">-WorkloadType</span></span>
<span data-ttu-id="1204d-129">리소스의 워크로드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-129">Workload type of the resource.</span></span> <span data-ttu-id="1204d-130">현재 지원되는 값은 AzureVM, WindowsServer, AzureFiles, MSSQL입니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="1204d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1204d-131">-Confirm</span></span>
<span data-ttu-id="1204d-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1204d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1204d-133">-WhatIf</span></span>
<span data-ttu-id="1204d-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1204d-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="1204d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1204d-135">CommonParameters</span></span>
<span data-ttu-id="1204d-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1204d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1204d-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1204d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1204d-138">입력</span><span class="sxs-lookup"><span data-stu-id="1204d-138">INPUTS</span></span>

### <span data-ttu-id="1204d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1204d-139">System.String</span></span>

## <span data-ttu-id="1204d-140">출력</span><span class="sxs-lookup"><span data-stu-id="1204d-140">OUTPUTS</span></span>

### <span data-ttu-id="1204d-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="1204d-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="1204d-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1204d-142">NOTES</span></span>

## <span data-ttu-id="1204d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1204d-143">RELATED LINKS</span></span>

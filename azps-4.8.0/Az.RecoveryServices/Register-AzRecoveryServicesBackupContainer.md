---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214251"
---
# <span data-ttu-id="09604-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="09604-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="09604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09604-102">SYNOPSIS</span></span>
<span data-ttu-id="09604-103">**AzRecoveryServicesBackupContainer** cmdlet은 특정 workloadType를 사용 하 여 azureworkloads 부하에 대 한 Azure VM을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="09604-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="09604-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09604-104">SYNTAX</span></span>

### <span data-ttu-id="09604-105">등록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="09604-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09604-106">다시</span><span class="sxs-lookup"><span data-stu-id="09604-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09604-107">설명은</span><span class="sxs-lookup"><span data-stu-id="09604-107">DESCRIPTION</span></span>
<span data-ttu-id="09604-108">이 명령을 사용 하면 Azure Backup이 리소스를 백업 컨테이너로 변환한 다음 지정 된 복구 서비스 자격 증명 모음에 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09604-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="09604-109">그런 다음 Azure Backup service는이 컨테이너 내에서 지정 된 작업 부하 유형의 작업을 나중에 보호 하도록 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09604-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="09604-110">예제의</span><span class="sxs-lookup"><span data-stu-id="09604-110">EXAMPLES</span></span>

### <span data-ttu-id="09604-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="09604-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="09604-112">Cmdlet은 azure VM을 작업 부하 MSSQL의 컨테이너로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="09604-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="09604-113">변수</span><span class="sxs-lookup"><span data-stu-id="09604-113">PARAMETERS</span></span>

### <span data-ttu-id="09604-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="09604-114">-BackupManagementType</span></span>
<span data-ttu-id="09604-115">보호 되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="09604-115">The class of resources being protected.</span></span> <span data-ttu-id="09604-116">현재이 cmdlet에 대해 지원 되는 값은 AzureWorkload 부하입니다.</span><span class="sxs-lookup"><span data-stu-id="09604-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="09604-117">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="09604-117">-Container</span></span>
<span data-ttu-id="09604-118">항목이 있는 컨테이너</span><span class="sxs-lookup"><span data-stu-id="09604-118">Container where the item resides</span></span>

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

### <span data-ttu-id="09604-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09604-119">-DefaultProfile</span></span>
<span data-ttu-id="09604-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09604-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09604-121">-Force</span><span class="sxs-lookup"><span data-stu-id="09604-121">-Force</span></span>
<span data-ttu-id="09604-122">강제로 레지스터 컨테이너를 만듭니다 (확인 대화 상자 방지).</span><span class="sxs-lookup"><span data-stu-id="09604-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="09604-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="09604-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="09604-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09604-124">-ResourceId</span></span>
<span data-ttu-id="09604-125">구독에서 일부 RecoveryServices 자격 증명 모음이 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="09604-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="09604-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="09604-126">-VaultId</span></span>
<span data-ttu-id="09604-127">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="09604-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="09604-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="09604-128">-WorkloadType</span></span>
<span data-ttu-id="09604-129">리소스의 작업 부하 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="09604-129">Workload type of the resource.</span></span> <span data-ttu-id="09604-130">현재 지원 되는 값은 Add-azurevm, WindowsServer, AzureFiles, MSSQL입니다.</span><span class="sxs-lookup"><span data-stu-id="09604-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="09604-131">-확인</span><span class="sxs-lookup"><span data-stu-id="09604-131">-Confirm</span></span>
<span data-ttu-id="09604-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09604-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09604-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09604-133">-WhatIf</span></span>
<span data-ttu-id="09604-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="09604-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="09604-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09604-135">CommonParameters</span></span>
<span data-ttu-id="09604-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09604-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09604-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09604-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09604-138">입력</span><span class="sxs-lookup"><span data-stu-id="09604-138">INPUTS</span></span>

### <span data-ttu-id="09604-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="09604-139">System.String</span></span>

## <span data-ttu-id="09604-140">출력</span><span class="sxs-lookup"><span data-stu-id="09604-140">OUTPUTS</span></span>

### <span data-ttu-id="09604-141">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="09604-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="09604-142">상속자</span><span class="sxs-lookup"><span data-stu-id="09604-142">NOTES</span></span>

## <span data-ttu-id="09604-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09604-143">RELATED LINKS</span></span>

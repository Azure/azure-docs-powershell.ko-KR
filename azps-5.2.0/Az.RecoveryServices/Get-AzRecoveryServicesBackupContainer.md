---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358800"
---
# <span data-ttu-id="693bc-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="693bc-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="693bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="693bc-102">SYNOPSIS</span></span>

<span data-ttu-id="693bc-103">Backup 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-103">Gets Backup containers.</span></span>

## <span data-ttu-id="693bc-104">구문</span><span class="sxs-lookup"><span data-stu-id="693bc-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="693bc-105">설명</span><span class="sxs-lookup"><span data-stu-id="693bc-105">DESCRIPTION</span></span>

<span data-ttu-id="693bc-106">**Get-AzRecoveryServicesBackupContainer** cmdlet은 백업 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="693bc-107">Backup 컨테이너는 백업 항목으로 모델링되는 데이터 원본을 캡슐화합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="693bc-108">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="693bc-109">예제</span><span class="sxs-lookup"><span data-stu-id="693bc-109">EXAMPLES</span></span>

### <span data-ttu-id="693bc-110">예제 1: 특정 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="693bc-111">이 명령은 AzureVM 형식의 V2VM이라는 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="693bc-112">예제 2: 특정 유형의 모든 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="693bc-113">이 명령은 Azure Backup 에이전트로 보호되는 모든 Windows 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="693bc-114">**BackupManagementType** 매개 변수는 Windows 컨테이너에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="693bc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="693bc-115">PARAMETERS</span></span>

### <span data-ttu-id="693bc-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="693bc-116">-BackupManagementType</span></span>

<span data-ttu-id="693bc-117">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-117">The class of resources being protected.</span></span> <span data-ttu-id="693bc-118">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="693bc-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="693bc-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="693bc-119">AzureVM</span></span>
- <span data-ttu-id="693bc-120">MARS</span><span class="sxs-lookup"><span data-stu-id="693bc-120">MARS</span></span>
- <span data-ttu-id="693bc-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="693bc-121">AzureWorkload</span></span>
- <span data-ttu-id="693bc-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="693bc-122">AzureStorage</span></span>

<span data-ttu-id="693bc-123">이 매개 변수는 MARS 에이전트 또는 다른 백업 엔진을 사용하여 백업된 Windows 컴퓨터를 차별화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693bc-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="693bc-124">-ContainerType</span></span>

<span data-ttu-id="693bc-125">백업 컨테이너 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-125">Specifies the backup container type.</span></span>
<span data-ttu-id="693bc-126">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="693bc-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="693bc-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="693bc-127">AzureVM</span></span>
- <span data-ttu-id="693bc-128">Windows</span><span class="sxs-lookup"><span data-stu-id="693bc-128">Windows</span></span>
- <span data-ttu-id="693bc-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="693bc-129">AzureSQL</span></span>
- <span data-ttu-id="693bc-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="693bc-130">AzureStorage</span></span>
- <span data-ttu-id="693bc-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="693bc-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693bc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693bc-132">-DefaultProfile</span></span>

<span data-ttu-id="693bc-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="693bc-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="693bc-134">-FriendlyName</span></span>

<span data-ttu-id="693bc-135">얻을 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-135">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693bc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="693bc-136">-ResourceGroupName</span></span>

<span data-ttu-id="693bc-137">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="693bc-138">이 매개 변수는 Azure 가상 머신에만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-138">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693bc-139">-Status</span><span class="sxs-lookup"><span data-stu-id="693bc-139">-Status</span></span>

<span data-ttu-id="693bc-140">컨테이너 등록 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-140">Specifies the container registration status.</span></span>
<span data-ttu-id="693bc-141">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="693bc-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="693bc-142">등록</span><span class="sxs-lookup"><span data-stu-id="693bc-142">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693bc-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="693bc-143">-VaultId</span></span>

<span data-ttu-id="693bc-144">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="693bc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693bc-145">CommonParameters</span></span>
<span data-ttu-id="693bc-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="693bc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693bc-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="693bc-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693bc-148">입력</span><span class="sxs-lookup"><span data-stu-id="693bc-148">INPUTS</span></span>

### <span data-ttu-id="693bc-149">System.String</span><span class="sxs-lookup"><span data-stu-id="693bc-149">System.String</span></span>

## <span data-ttu-id="693bc-150">출력</span><span class="sxs-lookup"><span data-stu-id="693bc-150">OUTPUTS</span></span>

### <span data-ttu-id="693bc-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="693bc-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="693bc-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="693bc-152">NOTES</span></span>

## <span data-ttu-id="693bc-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="693bc-153">RELATED LINKS</span></span>

[<span data-ttu-id="693bc-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="693bc-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="693bc-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="693bc-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="693bc-156">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="693bc-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

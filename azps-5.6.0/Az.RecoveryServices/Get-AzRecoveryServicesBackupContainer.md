---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 0fb1df2d72259c6c0f427a9a66f4cf271cc0cbfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984288"
---
# <span data-ttu-id="aab60-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="aab60-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="aab60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab60-102">SYNOPSIS</span></span>

<span data-ttu-id="aab60-103">Backup 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-103">Gets Backup containers.</span></span>

## <span data-ttu-id="aab60-104">구문</span><span class="sxs-lookup"><span data-stu-id="aab60-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aab60-105">설명</span><span class="sxs-lookup"><span data-stu-id="aab60-105">DESCRIPTION</span></span>

<span data-ttu-id="aab60-106">**Get-AzRecoveryServicesBackupContainer** cmdlet은 백업 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="aab60-107">Backup 컨테이너는 백업 항목으로 모델링된 데이터 원본을 캡슐화합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="aab60-108">컨테이너 형식 "Azure VM"의 경우 출력은 이름이 친숙한 이름 매개 변수의 값으로 전달된 컨테이너와 정확히 일치하는 모든 컨테이너를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="aab60-109">다른 컨테이너 형식의 경우 출력은 친숙 이름 매개 변수에 전달된 값과 비슷한 이름을 사용하는 컨테이너 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="aab60-110">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="aab60-111">예제</span><span class="sxs-lookup"><span data-stu-id="aab60-111">EXAMPLES</span></span>

### <span data-ttu-id="aab60-112">예제 1: 특정 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="aab60-113">이 명령은 AzureVM 형식의 V2VM이라는 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="aab60-114">예제 2: 특정 유형의 모든 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="aab60-115">이 명령은 Azure Backup 에이전트에 의해 보호되는 모든 Windows 컨테이너를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="aab60-116">**BackupManagementType** 매개 변수는 Windows 컨테이너에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="aab60-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aab60-117">PARAMETERS</span></span>

### <span data-ttu-id="aab60-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="aab60-118">-BackupManagementType</span></span>

<span data-ttu-id="aab60-119">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-119">The class of resources being protected.</span></span> <span data-ttu-id="aab60-120">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aab60-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="aab60-121">AzureVM</span></span>
- <span data-ttu-id="aab60-122">MARS</span><span class="sxs-lookup"><span data-stu-id="aab60-122">MARS</span></span>
- <span data-ttu-id="aab60-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="aab60-123">AzureWorkload</span></span>
- <span data-ttu-id="aab60-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="aab60-124">AzureStorage</span></span>

<span data-ttu-id="aab60-125">이 매개 변수는 MARS 에이전트 또는 기타 백업 엔진을 사용하여 백업된 Windows 컴퓨터를 차별화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="aab60-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="aab60-126">-ContainerType</span></span>

<span data-ttu-id="aab60-127">백업 컨테이너 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-127">Specifies the backup container type.</span></span>
<span data-ttu-id="aab60-128">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aab60-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="aab60-129">AzureVM</span></span>
- <span data-ttu-id="aab60-130">Windows</span><span class="sxs-lookup"><span data-stu-id="aab60-130">Windows</span></span>
- <span data-ttu-id="aab60-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="aab60-131">AzureStorage</span></span>
- <span data-ttu-id="aab60-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="aab60-132">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab60-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab60-133">-DefaultProfile</span></span>

<span data-ttu-id="aab60-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aab60-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="aab60-135">-FriendlyName</span></span>

<span data-ttu-id="aab60-136">얻을 컨테이너의 친숙한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="aab60-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab60-137">-ResourceGroupName</span></span>

<span data-ttu-id="aab60-138">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="aab60-139">이 매개 변수는 Azure 가상 머신에만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="aab60-140">-Status</span><span class="sxs-lookup"><span data-stu-id="aab60-140">-Status</span></span>

<span data-ttu-id="aab60-141">컨테이너 등록 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-141">Specifies the container registration status.</span></span>
<span data-ttu-id="aab60-142">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aab60-143">등록된</span><span class="sxs-lookup"><span data-stu-id="aab60-143">Registered</span></span>

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

### <span data-ttu-id="aab60-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="aab60-144">-VaultId</span></span>

<span data-ttu-id="aab60-145">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="aab60-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab60-146">CommonParameters</span></span>
<span data-ttu-id="aab60-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aab60-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab60-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aab60-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab60-149">입력</span><span class="sxs-lookup"><span data-stu-id="aab60-149">INPUTS</span></span>

### <span data-ttu-id="aab60-150">System.String</span><span class="sxs-lookup"><span data-stu-id="aab60-150">System.String</span></span>

## <span data-ttu-id="aab60-151">출력</span><span class="sxs-lookup"><span data-stu-id="aab60-151">OUTPUTS</span></span>

### <span data-ttu-id="aab60-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="aab60-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="aab60-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aab60-153">NOTES</span></span>

## <span data-ttu-id="aab60-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aab60-154">RELATED LINKS</span></span>

[<span data-ttu-id="aab60-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="aab60-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="aab60-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="aab60-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="aab60-157">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="aab60-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

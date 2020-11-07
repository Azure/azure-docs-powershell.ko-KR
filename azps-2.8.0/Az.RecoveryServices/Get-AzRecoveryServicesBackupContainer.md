---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 342ee52cf0e5e0f94c8b57b4e4cf0e798abbf0fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872714"
---
# <span data-ttu-id="06ce3-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="06ce3-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="06ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06ce3-102">SYNOPSIS</span></span>

<span data-ttu-id="06ce3-103">백업 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-103">Gets Backup containers.</span></span>

## <span data-ttu-id="06ce3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06ce3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06ce3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06ce3-105">DESCRIPTION</span></span>

<span data-ttu-id="06ce3-106">**Get-AzRecoveryServicesBackupContainer** cmdlet은 백업 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="06ce3-107">백업 컨테이너는 백업 항목으로 modelled 된 데이터 원본을 캡슐화 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="06ce3-108">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="06ce3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="06ce3-109">EXAMPLES</span></span>

### <span data-ttu-id="06ce3-110">예제 1: 특정 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="06ce3-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="06ce3-111">이 명령은 Add-azurevm 유형의 V2VM 이라는 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="06ce3-112">예제 2: 특정 형식의 모든 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="06ce3-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="06ce3-113">이 명령은 Azure Backup agent로 보호 되는 모든 Windows 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="06ce3-114">**Backupmanagementtype** 매개 변수는 Windows 컨테이너에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="06ce3-115">변수</span><span class="sxs-lookup"><span data-stu-id="06ce3-115">PARAMETERS</span></span>

### <span data-ttu-id="06ce3-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="06ce3-116">-BackupManagementType</span></span>

<span data-ttu-id="06ce3-117">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-117">Specifies the backup management type.</span></span>
<span data-ttu-id="06ce3-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06ce3-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="06ce3-119">AzureVM</span></span>
- <span data-ttu-id="06ce3-120">화성</span><span class="sxs-lookup"><span data-stu-id="06ce3-120">MARS</span></span>
- <span data-ttu-id="06ce3-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="06ce3-121">AzureSQL</span></span>
- <span data-ttu-id="06ce3-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="06ce3-122">AzureStorage</span></span>

<span data-ttu-id="06ce3-123">이 매개 변수는 MARS 에이전트 또는 다른 백업 엔진을 사용 하 여 백업 되는 Windows 컴퓨터를 구분 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ce3-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="06ce3-124">-ContainerType</span></span>

<span data-ttu-id="06ce3-125">백업 컨테이너 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-125">Specifies the backup container type.</span></span>
<span data-ttu-id="06ce3-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06ce3-127">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="06ce3-127">AzureVM</span></span>
- <span data-ttu-id="06ce3-128">창을</span><span class="sxs-lookup"><span data-stu-id="06ce3-128">Windows</span></span>
- <span data-ttu-id="06ce3-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="06ce3-129">AzureSQL</span></span>
- <span data-ttu-id="06ce3-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="06ce3-130">AzureStorage</span></span>
- <span data-ttu-id="06ce3-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="06ce3-131">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="06ce3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ce3-132">-DefaultProfile</span></span>

<span data-ttu-id="06ce3-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06ce3-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="06ce3-134">-FriendlyName</span></span>

<span data-ttu-id="06ce3-135">가져올 컨테이너의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="06ce3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ce3-136">-ResourceGroupName</span></span>

<span data-ttu-id="06ce3-137">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="06ce3-138">이 매개 변수는 Azure 가상 머신에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="06ce3-139">-상태</span><span class="sxs-lookup"><span data-stu-id="06ce3-139">-Status</span></span>

<span data-ttu-id="06ce3-140">컨테이너 등록 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-140">Specifies the container registration status.</span></span>
<span data-ttu-id="06ce3-141">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06ce3-142">되어</span><span class="sxs-lookup"><span data-stu-id="06ce3-142">Registered</span></span>

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

### <span data-ttu-id="06ce3-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="06ce3-143">-VaultId</span></span>

<span data-ttu-id="06ce3-144">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="06ce3-145">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ce3-145">-CommonParameters</span></span>

<span data-ttu-id="06ce3-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06ce3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ce3-147">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06ce3-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ce3-148">입력</span><span class="sxs-lookup"><span data-stu-id="06ce3-148">INPUTS</span></span>

### <span data-ttu-id="06ce3-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06ce3-149">System.String</span></span>

## <span data-ttu-id="06ce3-150">출력</span><span class="sxs-lookup"><span data-stu-id="06ce3-150">OUTPUTS</span></span>

### <span data-ttu-id="06ce3-151">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="06ce3-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="06ce3-152">상속자</span><span class="sxs-lookup"><span data-stu-id="06ce3-152">NOTES</span></span>

## <span data-ttu-id="06ce3-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06ce3-153">RELATED LINKS</span></span>

[<span data-ttu-id="06ce3-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="06ce3-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="06ce3-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="06ce3-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="06ce3-156">등록 취소-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="06ce3-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703817"
---
# <span data-ttu-id="5c06f-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="5c06f-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="5c06f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c06f-102">SYNOPSIS</span></span>
<span data-ttu-id="5c06f-103">백업 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c06f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c06f-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c06f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c06f-105">DESCRIPTION</span></span>
<span data-ttu-id="5c06f-106">**Get-AzureRmRecoveryServicesBackupContainer** cmdlet은 백업 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="5c06f-107">백업 컨테이너는 백업 항목으로 modelled 된 데이터 원본을 캡슐화 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="5c06f-108">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5c06f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5c06f-109">EXAMPLES</span></span>

### <span data-ttu-id="5c06f-110">예제 1: 특정 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c06f-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="5c06f-111">이 명령은 Add-azurevm 유형의 V2VM 이라는 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="5c06f-112">예제 2: 특정 형식의 모든 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c06f-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="5c06f-113">이 명령은 Azure Backup agent로 보호 되는 모든 Windows 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="5c06f-114">*Backupmanagementtype* 매개 변수는 Windows 컨테이너에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="5c06f-115">변수</span><span class="sxs-lookup"><span data-stu-id="5c06f-115">PARAMETERS</span></span>

### <span data-ttu-id="5c06f-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5c06f-116">-BackupManagementType</span></span>
<span data-ttu-id="5c06f-117">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-117">Specifies the backup management type.</span></span>
<span data-ttu-id="5c06f-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c06f-119">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="5c06f-119">AzureVM</span></span>
- <span data-ttu-id="5c06f-120">화성</span><span class="sxs-lookup"><span data-stu-id="5c06f-120">MARS</span></span>
- <span data-ttu-id="5c06f-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="5c06f-121">AzureSQL</span></span>
- <span data-ttu-id="5c06f-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="5c06f-122">AzureStorage</span></span>

<span data-ttu-id="5c06f-123">이 매개 변수는 MARS 에이전트 또는 다른 백업 엔진을 사용 하 여 백업 되는 Windows 컴퓨터를 구분 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="5c06f-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="5c06f-124">-ContainerType</span></span>
<span data-ttu-id="5c06f-125">백업 컨테이너 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-125">Specifies the backup container type.</span></span>
<span data-ttu-id="5c06f-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c06f-127">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="5c06f-127">AzureVM</span></span> 
- <span data-ttu-id="5c06f-128">창을</span><span class="sxs-lookup"><span data-stu-id="5c06f-128">Windows</span></span>
- <span data-ttu-id="5c06f-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="5c06f-129">AzureSQL</span></span>
- <span data-ttu-id="5c06f-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="5c06f-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c06f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c06f-131">-DefaultProfile</span></span>
<span data-ttu-id="5c06f-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c06f-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5c06f-133">-FriendlyName</span></span>
<span data-ttu-id="5c06f-134">가져올 컨테이너의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="5c06f-135">-이름</span><span class="sxs-lookup"><span data-stu-id="5c06f-135">-Name</span></span>
<span data-ttu-id="5c06f-136">가져올 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-136">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="5c06f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c06f-137">-ResourceGroupName</span></span>
<span data-ttu-id="5c06f-138">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="5c06f-139">이 매개 변수는 Azure 가상 머신에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="5c06f-140">-상태</span><span class="sxs-lookup"><span data-stu-id="5c06f-140">-Status</span></span>
<span data-ttu-id="5c06f-141">컨테이너 등록 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-141">Specifies the container registration status.</span></span>
<span data-ttu-id="5c06f-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c06f-143">되어</span><span class="sxs-lookup"><span data-stu-id="5c06f-143">Registered</span></span>

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

### <span data-ttu-id="5c06f-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5c06f-144">-VaultId</span></span>
<span data-ttu-id="5c06f-145">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5c06f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c06f-146">CommonParameters</span></span>
<span data-ttu-id="5c06f-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c06f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c06f-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c06f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c06f-149">입력</span><span class="sxs-lookup"><span data-stu-id="5c06f-149">INPUTS</span></span>

### <span data-ttu-id="5c06f-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5c06f-150">System.String</span></span>
<span data-ttu-id="5c06f-151">매개 변수: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5c06f-151">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="5c06f-152">출력</span><span class="sxs-lookup"><span data-stu-id="5c06f-152">OUTPUTS</span></span>

### <span data-ttu-id="5c06f-153">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="5c06f-153">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="5c06f-154">상속자</span><span class="sxs-lookup"><span data-stu-id="5c06f-154">NOTES</span></span>

## <span data-ttu-id="5c06f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c06f-155">RELATED LINKS</span></span>

[<span data-ttu-id="5c06f-156">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5c06f-156">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5c06f-157">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="5c06f-157">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="5c06f-158">등록 취소-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="5c06f-158">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)



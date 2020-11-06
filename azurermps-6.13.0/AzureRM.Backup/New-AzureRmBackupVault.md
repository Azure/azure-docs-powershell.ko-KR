---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: ad3619d2d0fcb9b60639a19b0c7d3fea45833857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531475"
---
# <span data-ttu-id="e62d2-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e62d2-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="e62d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e62d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e62d2-103">백업 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e62d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e62d2-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e62d2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e62d2-105">DESCRIPTION</span></span>
<span data-ttu-id="e62d2-106">**AzureRmBackupVault** Cmdlet은 Azure Backup 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="e62d2-107">이 cmdlet은 자격 증명 모음 엔터티에 대 한 참조 역할을 하는 **AzureRmBackupVault** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="e62d2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e62d2-108">EXAMPLES</span></span>

### <span data-ttu-id="e62d2-109">예제 1: 백업 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="e62d2-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="e62d2-110">이 명령은 Vault03 이라는 Azure 백업 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="e62d2-111">자격 증명 모음이 미국 지역의 ResourceGroup01 이라는 리소스 그룹에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="e62d2-112">자격 증명 모음에서는 기본 GeoRedundant 저장소 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="e62d2-113">예제 2: 로컬에서 중복 저장소를 사용 하는 백업 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="e62d2-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="e62d2-114">이 명령은 Vault03 이라는 Azure 백업 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="e62d2-115">자격 증명 모음이 미국 지역의 ResourceGroup02 이라는 리소스 그룹에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="e62d2-116">자격 증명 모음이 LocallyRedundant 저장소 유형을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="e62d2-117">변수</span><span class="sxs-lookup"><span data-stu-id="e62d2-117">PARAMETERS</span></span>

### <span data-ttu-id="e62d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62d2-118">-DefaultProfile</span></span>
<span data-ttu-id="e62d2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e62d2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e62d2-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e62d2-120">-Name</span></span>
<span data-ttu-id="e62d2-121">Azure Backup vault의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-121">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="e62d2-122">이름은 리소스 그룹에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-122">The name must be unique in a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62d2-123">-지역</span><span class="sxs-lookup"><span data-stu-id="e62d2-123">-Region</span></span>
<span data-ttu-id="e62d2-124">백업 자격 증명 모음이 존재 하는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-124">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="e62d2-125">하이브리드 백업 시나리오의 경우 대기 시간을 줄이기 위해 온-프레미스 서버 가까이에 있는 영역에 자격 증명 모음을 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-125">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="e62d2-126">Azure 인프라를 서비스 (IaaS) 가상 컴퓨터로 백업 하는 경우 자격 증명 모음이 로컬 가상 컴퓨터에 대 한 검색 지점이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-126">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62d2-127">-ResourceGroupName</span></span>
<span data-ttu-id="e62d2-128">이 cmdlet이 백업 자격 증명 모음을 만드는 기존 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-128">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="e62d2-129">리소스 그룹을 만들려면 New-AzureRMResourceGroup cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-129">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="e62d2-130">리소스 그룹과 Azure Backup 자격 증명 모음이 동일한 지역에 있을 필요는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-130">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62d2-131">-저장소</span><span class="sxs-lookup"><span data-stu-id="e62d2-131">-Storage</span></span>
<span data-ttu-id="e62d2-132">백업 데이터의 저장소 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-132">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="e62d2-133">이 매개 변수에 허용 되는 값은 LocallyRedundant 및 GeoRedundant입니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-133">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="e62d2-134">기본 값은 GeoRedundant입니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-134">The default value is GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62d2-135">CommonParameters</span></span>
<span data-ttu-id="e62d2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e62d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62d2-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e62d2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62d2-138">입력</span><span class="sxs-lookup"><span data-stu-id="e62d2-138">INPUTS</span></span>

### <span data-ttu-id="e62d2-139">않아야</span><span class="sxs-lookup"><span data-stu-id="e62d2-139">None</span></span>

## <span data-ttu-id="e62d2-140">출력</span><span class="sxs-lookup"><span data-stu-id="e62d2-140">OUTPUTS</span></span>

### <span data-ttu-id="e62d2-141">AzureRMBackupVault를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="e62d2-141">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="e62d2-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e62d2-142">NOTES</span></span>
* <span data-ttu-id="e62d2-143">않아야</span><span class="sxs-lookup"><span data-stu-id="e62d2-143">None</span></span>

## <span data-ttu-id="e62d2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e62d2-144">RELATED LINKS</span></span>

[<span data-ttu-id="e62d2-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e62d2-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="e62d2-146">제거-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e62d2-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="e62d2-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e62d2-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)



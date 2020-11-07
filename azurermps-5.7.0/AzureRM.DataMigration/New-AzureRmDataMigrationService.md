---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711175"
---
# <span data-ttu-id="5b231-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5b231-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="5b231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b231-102">SYNOPSIS</span></span>
<span data-ttu-id="5b231-103">Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b231-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b231-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="5b231-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b231-105">DESCRIPTION</span></span>
<span data-ttu-id="5b231-106">New-AzureRmDataMigrationService cmdlet은 Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="5b231-107">이 cmdlet은 기존 Azure 리소스 그룹의 이름, 만들려는 Azure Database 마이그레이션 서비스의 새 인스턴스에 대 한 고유 이름, 인스턴스가 프로 비전 된 지역, DMS 작업자 SKU의 이름, 서비스를 상주할 Azure 가상 서브넷의 이름에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="5b231-108">구독 이름에 대 한 매개 변수는 사용자가 Azure 로그인 세션의 기본 구독을 지정 하거나 실행 Get-AzureRmSubscription – SubscriptionName "MySubscription" | 다른 구독을 선택 Select-AzureRmSubscription.</span><span class="sxs-lookup"><span data-stu-id="5b231-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription –SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="5b231-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5b231-109">EXAMPLES</span></span>

### <span data-ttu-id="5b231-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b231-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="5b231-111">위 예제에서는 중앙 US 지역에서 TestService 라는 Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>


## <span data-ttu-id="5b231-112">변수</span><span class="sxs-lookup"><span data-stu-id="5b231-112">PARAMETERS</span></span>

### <span data-ttu-id="5b231-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b231-113">-DefaultProfile</span></span>
<span data-ttu-id="5b231-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b231-115">-위치</span><span class="sxs-lookup"><span data-stu-id="5b231-115">-Location</span></span>
<span data-ttu-id="5b231-116">만들 Azure 데이터베이스 마이그레이션 서비스 인스턴스의 위치 이며, Azure 지역에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b231-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b231-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b231-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b231-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5b231-119">-ServiceName</span></span>
<span data-ttu-id="5b231-120">Azure 데이터베이스 마이그레이션 서비스 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-120">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b231-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="5b231-121">-Sku</span></span>
<span data-ttu-id="5b231-122">Azure 데이터베이스 마이그레이션 서비스 인스턴스의 sku입니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="5b231-123">사용할 수 있는 값은 현재 Basic_1vCore, Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="5b231-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b231-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="5b231-124">-VirtualSubnetId</span></span>
<span data-ttu-id="5b231-125">Azure 데이터베이스 마이그레이션 서비스 인스턴스에 사용할 지정 된 가상 네트워크 아래 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b231-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="5b231-126">출력</span><span class="sxs-lookup"><span data-stu-id="5b231-126">OUTPUTS</span></span>

### <span data-ttu-id="5b231-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="5b231-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>


## <span data-ttu-id="5b231-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5b231-128">NOTES</span></span>

## <span data-ttu-id="5b231-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b231-129">RELATED LINKS</span></span>


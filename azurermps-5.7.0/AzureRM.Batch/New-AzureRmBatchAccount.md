---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: c4a8eb0bc75660c13ce8f8492b72cce8a77280e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529942"
---
# <span data-ttu-id="75d6d-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75d6d-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="75d6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="75d6d-103">일괄 처리 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75d6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75d6d-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d6d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75d6d-105">DESCRIPTION</span></span>
<span data-ttu-id="75d6d-106">**AzureRmBatchAccount** cmdlet은 지정 된 리소스 그룹 및 위치에 대 한 Azure Batch 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="75d6d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="75d6d-107">EXAMPLES</span></span>

### <span data-ttu-id="75d6d-108">예제 1: 일괄 처리 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="75d6d-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="75d6d-109">이 명령은 미국 내 위치에서 ResourceGroup03 리소스 그룹을 사용 하 여 pfuller 이라는 일괄 처리 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="75d6d-110">변수</span><span class="sxs-lookup"><span data-stu-id="75d6d-110">PARAMETERS</span></span>

### <span data-ttu-id="75d6d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75d6d-111">-AccountName</span></span>
<span data-ttu-id="75d6d-112">이 cmdlet이 만드는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="75d6d-113">일괄 처리 계정 이름은 3 ~ 24 자 사이 여야 하며 숫자와 소문자만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6d-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="75d6d-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="75d6d-115">자동 저장소에 사용 되는 저장소 계정의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d6d-116">-DefaultProfile</span></span>
<span data-ttu-id="75d6d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75d6d-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="75d6d-118">-KeyVaultId</span></span>
<span data-ttu-id="75d6d-119">일괄 처리 계정과 연결 된 Azure 키 자격 증명 모음의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6d-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="75d6d-120">-KeyVaultUrl</span></span>
<span data-ttu-id="75d6d-121">일괄 처리 계정과 연결 된 Azure 키 보관소의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-121">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6d-122">-위치</span><span class="sxs-lookup"><span data-stu-id="75d6d-122">-Location</span></span>
<span data-ttu-id="75d6d-123">이 cmdlet이 계정을 만드는 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="75d6d-124">자세한 내용은 [Azure 지역을](https://azure.microsoft.com/en-us/regions)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="75d6d-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6d-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="75d6d-125">-PoolAllocationMode</span></span>
<span data-ttu-id="75d6d-126">Batch 계정에서 풀을 만들기 위한 배정 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: PoolAllocationMode
Parameter Sets: (All)
Aliases: 
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d6d-127">-ResourceGroupName</span></span>
<span data-ttu-id="75d6d-128">이 cmdlet이 계정을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6d-129">태그</span><span class="sxs-lookup"><span data-stu-id="75d6d-129">-Tag</span></span>
<span data-ttu-id="75d6d-130">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75d6d-131">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="75d6d-131">For example:</span></span>

<span data-ttu-id="75d6d-132">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="75d6d-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d6d-133">CommonParameters</span></span>
<span data-ttu-id="75d6d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d6d-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d6d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d6d-136">입력</span><span class="sxs-lookup"><span data-stu-id="75d6d-136">INPUTS</span></span>

### <span data-ttu-id="75d6d-137">않아야</span><span class="sxs-lookup"><span data-stu-id="75d6d-137">None</span></span>
<span data-ttu-id="75d6d-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75d6d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75d6d-139">출력</span><span class="sxs-lookup"><span data-stu-id="75d6d-139">OUTPUTS</span></span>

### <span data-ttu-id="75d6d-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="75d6d-140">BatchAccountContext</span></span>

## <span data-ttu-id="75d6d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="75d6d-141">NOTES</span></span>

## <span data-ttu-id="75d6d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75d6d-142">RELATED LINKS</span></span>

[<span data-ttu-id="75d6d-143">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75d6d-143">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="75d6d-144">제거-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75d6d-144">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="75d6d-145">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75d6d-145">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="75d6d-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="75d6d-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

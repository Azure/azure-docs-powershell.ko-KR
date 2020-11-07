---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: ed44fa5960935bbe353d775a426e023512327e7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702771"
---
# <span data-ttu-id="44f20-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="44f20-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="44f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44f20-102">SYNOPSIS</span></span>
<span data-ttu-id="44f20-103">일괄 처리 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44f20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44f20-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44f20-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44f20-105">DESCRIPTION</span></span>
<span data-ttu-id="44f20-106">**AzureRmBatchAccount** cmdlet은 지정 된 리소스 그룹 및 위치에 대 한 Azure Batch 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="44f20-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44f20-107">EXAMPLES</span></span>

### <span data-ttu-id="44f20-108">예제 1: 일괄 처리 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="44f20-108">Example 1: Create a Batch account</span></span>
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

<span data-ttu-id="44f20-109">이 명령은 미국 내 위치에서 ResourceGroup03 리소스 그룹을 사용 하 여 pfuller 이라는 일괄 처리 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="44f20-110">변수</span><span class="sxs-lookup"><span data-stu-id="44f20-110">PARAMETERS</span></span>

### <span data-ttu-id="44f20-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="44f20-111">-AccountName</span></span>
<span data-ttu-id="44f20-112">이 cmdlet이 만드는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="44f20-113">일괄 처리 계정 이름은 3 ~ 24 자 사이 여야 하며 숫자와 소문자만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f20-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="44f20-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="44f20-115">자동 저장소에 사용 되는 저장소 계정의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f20-116">-위치</span><span class="sxs-lookup"><span data-stu-id="44f20-116">-Location</span></span>
<span data-ttu-id="44f20-117">이 cmdlet이 계정을 만드는 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-117">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="44f20-118">자세한 내용은 [Azure 지역을](https://azure.microsoft.com/en-us/regions)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="44f20-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f20-119">-ResourceGroupName</span></span>
<span data-ttu-id="44f20-120">이 cmdlet이 계정을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-120">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f20-121">태그</span><span class="sxs-lookup"><span data-stu-id="44f20-121">-Tag</span></span>
<span data-ttu-id="44f20-122">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="44f20-123">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="44f20-123">For example:</span></span>

<span data-ttu-id="44f20-124">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="44f20-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f20-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f20-125">-DefaultProfile</span></span>
<span data-ttu-id="44f20-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44f20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f20-127">CommonParameters</span></span>
<span data-ttu-id="44f20-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44f20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f20-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44f20-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f20-130">입력</span><span class="sxs-lookup"><span data-stu-id="44f20-130">INPUTS</span></span>

## <span data-ttu-id="44f20-131">출력</span><span class="sxs-lookup"><span data-stu-id="44f20-131">OUTPUTS</span></span>

### <span data-ttu-id="44f20-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="44f20-132">BatchAccountContext</span></span>

## <span data-ttu-id="44f20-133">상속자</span><span class="sxs-lookup"><span data-stu-id="44f20-133">NOTES</span></span>

## <span data-ttu-id="44f20-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44f20-134">RELATED LINKS</span></span>

[<span data-ttu-id="44f20-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="44f20-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="44f20-136">제거-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="44f20-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="44f20-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="44f20-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="44f20-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="44f20-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 7fd0283860fd5a0bbca1376afff00c8d4add29b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527084"
---
# <span data-ttu-id="a38dc-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a38dc-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="a38dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a38dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a38dc-103">현재 구독에서 일괄 처리 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a38dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a38dc-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a38dc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a38dc-105">DESCRIPTION</span></span>
<span data-ttu-id="a38dc-106">**AzureRmBatchAccount** cmdlet은 현재 구독에서 Azure Batch 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="a38dc-107">*AccountName* 매개 변수를 사용 하 여 단일 계정을 가져올 수도 있고, *ResourceGroupName* 매개 변수를 사용 하 여 해당 리소스 그룹 아래에 계정을 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="a38dc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a38dc-108">EXAMPLES</span></span>

### <span data-ttu-id="a38dc-109">예제 1: 이름으로 일괄 처리 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="a38dc-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="a38dc-110">이 명령은 pfuller 이름의 일괄 처리 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="a38dc-111">예제 2: 리소스 그룹과 연결 된 일괄 처리 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="a38dc-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="a38dc-112">이 명령은 CmdletExampleRG 리소스 그룹과 연결 된 일괄 처리 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="a38dc-113">변수</span><span class="sxs-lookup"><span data-stu-id="a38dc-113">PARAMETERS</span></span>

### <span data-ttu-id="a38dc-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a38dc-114">-AccountName</span></span>
<span data-ttu-id="a38dc-115">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-115">Specifies the name of an account.</span></span>
<span data-ttu-id="a38dc-116">계정 이름을 지정 하면이 cmdlet은 해당 계정만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a38dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a38dc-117">-DefaultProfile</span></span>
<span data-ttu-id="a38dc-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a38dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a38dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="a38dc-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a38dc-121">리소스 그룹을 지정 하는 경우이 cmdlet은 지정 된 리소스 그룹의 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a38dc-122">태그</span><span class="sxs-lookup"><span data-stu-id="a38dc-122">-Tag</span></span>
<span data-ttu-id="a38dc-123">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a38dc-124">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a38dc-124">For example:</span></span>

<span data-ttu-id="a38dc-125">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a38dc-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="a38dc-126">이 cmdlet은이 매개 변수에서 지정 하는 태그가 포함 된 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-126">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a38dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a38dc-127">CommonParameters</span></span>
<span data-ttu-id="a38dc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a38dc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a38dc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a38dc-130">입력</span><span class="sxs-lookup"><span data-stu-id="a38dc-130">INPUTS</span></span>

### <span data-ttu-id="a38dc-131">않아야</span><span class="sxs-lookup"><span data-stu-id="a38dc-131">None</span></span>
<span data-ttu-id="a38dc-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a38dc-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a38dc-133">출력</span><span class="sxs-lookup"><span data-stu-id="a38dc-133">OUTPUTS</span></span>

### <span data-ttu-id="a38dc-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a38dc-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a38dc-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a38dc-135">NOTES</span></span>

## <span data-ttu-id="a38dc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a38dc-136">RELATED LINKS</span></span>

[<span data-ttu-id="a38dc-137">새로운 AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a38dc-137">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="a38dc-138">제거-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a38dc-138">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="a38dc-139">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a38dc-139">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="a38dc-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a38dc-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

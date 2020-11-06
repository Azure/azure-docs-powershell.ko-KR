---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: ddc3bab48e766f80375fdf98add15e16e0086fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526319"
---
# <span data-ttu-id="a3893-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a3893-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="a3893-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3893-102">SYNOPSIS</span></span>
<span data-ttu-id="a3893-103">현재 구독에서 일괄 처리 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3893-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3893-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3893-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3893-105">DESCRIPTION</span></span>
<span data-ttu-id="a3893-106">**AzureRmBatchAccount** cmdlet은 현재 구독에서 Azure Batch 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="a3893-107">*AccountName* 매개 변수를 사용 하 여 단일 계정을 가져올 수도 있고, *ResourceGroupName* 매개 변수를 사용 하 여 해당 리소스 그룹 아래에 계정을 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="a3893-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a3893-108">EXAMPLES</span></span>

### <span data-ttu-id="a3893-109">예제 1: 이름으로 일괄 처리 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="a3893-109">Example 1: Get a batch account by name</span></span>
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

<span data-ttu-id="a3893-110">이 명령은 pfuller 이름의 일괄 처리 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="a3893-111">예제 2: 리소스 그룹과 연결 된 일괄 처리 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="a3893-111">Example 2: Get the batch accounts associated with a resource group</span></span>
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

<span data-ttu-id="a3893-112">이 명령은 CmdletExampleRG 리소스 그룹과 연결 된 일괄 처리 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="a3893-113">변수</span><span class="sxs-lookup"><span data-stu-id="a3893-113">PARAMETERS</span></span>

### <span data-ttu-id="a3893-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3893-114">-AccountName</span></span>
<span data-ttu-id="a3893-115">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-115">Specifies the name of an account.</span></span>
<span data-ttu-id="a3893-116">계정 이름을 지정 하면이 cmdlet은 해당 계정만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3893-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3893-117">-DefaultProfile</span></span>
<span data-ttu-id="a3893-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3893-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3893-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3893-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a3893-121">리소스 그룹을 지정 하는 경우이 cmdlet은 지정 된 리소스 그룹의 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3893-122">태그</span><span class="sxs-lookup"><span data-stu-id="a3893-122">-Tag</span></span>
<span data-ttu-id="a3893-123">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a3893-124">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}이 cmdlet은이 매개 변수에서 지정 하는 태그를 포함 하는 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3893-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3893-125">CommonParameters</span></span>
<span data-ttu-id="a3893-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3893-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3893-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3893-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3893-128">입력</span><span class="sxs-lookup"><span data-stu-id="a3893-128">INPUTS</span></span>

### <span data-ttu-id="a3893-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a3893-129">System.String</span></span>

### <span data-ttu-id="a3893-130">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="a3893-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a3893-131">출력</span><span class="sxs-lookup"><span data-stu-id="a3893-131">OUTPUTS</span></span>

### <span data-ttu-id="a3893-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a3893-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a3893-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a3893-133">NOTES</span></span>

## <span data-ttu-id="a3893-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3893-134">RELATED LINKS</span></span>

[<span data-ttu-id="a3893-135">새로운 AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a3893-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="a3893-136">제거-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a3893-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="a3893-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a3893-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="a3893-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a3893-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

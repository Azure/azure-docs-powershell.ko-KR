---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 66bab11ab5632464eed8ee160df527b0e44f053d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373010"
---
# <span data-ttu-id="1bbae-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1bbae-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="1bbae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bbae-102">SYNOPSIS</span></span>
<span data-ttu-id="1bbae-103">현재 구독에서 Batch 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="1bbae-104">구문</span><span class="sxs-lookup"><span data-stu-id="1bbae-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bbae-105">설명</span><span class="sxs-lookup"><span data-stu-id="1bbae-105">DESCRIPTION</span></span>
<span data-ttu-id="1bbae-106">**Get-AzBatchAccount** cmdlet은 현재 구독에서 Azure Batch 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="1bbae-107">*AccountName* 매개 변수를 사용하여 단일 계정을 얻거나 *ResourceGroupName* 매개 변수를 사용하여 해당 리소스 그룹에서 계정을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="1bbae-108">예제</span><span class="sxs-lookup"><span data-stu-id="1bbae-108">EXAMPLES</span></span>

### <span data-ttu-id="1bbae-109">예제 1: 이름에 따라 일괄 처리 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="1bbae-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="1bbae-110">이 명령은 pfuller라는 일괄 처리 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="1bbae-111">예제 2: 리소스 그룹과 연결된 배치 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="1bbae-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="1bbae-112">이 명령은 CmdletExampleRG 리소스 그룹과 연결된 배치 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="1bbae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bbae-113">PARAMETERS</span></span>

### <span data-ttu-id="1bbae-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1bbae-114">-AccountName</span></span>
<span data-ttu-id="1bbae-115">계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-115">Specifies the name of an account.</span></span>
<span data-ttu-id="1bbae-116">계정 이름을 지정하는 경우 이 cmdlet은 해당 계정만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="1bbae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bbae-117">-DefaultProfile</span></span>
<span data-ttu-id="1bbae-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bbae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bbae-119">-ResourceGroupName</span></span>
<span data-ttu-id="1bbae-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1bbae-121">리소스 그룹을 지정하는 경우 이 cmdlet은 지정된 리소스 그룹에서 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="1bbae-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bbae-122">-Tag</span></span>
<span data-ttu-id="1bbae-123">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1bbae-124">예: @{key0="value0";key1=$null;key2="value2"} 이 cmdlet은 이 매개 변수가 지정하는 태그를 포함하는 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="1bbae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bbae-125">CommonParameters</span></span>
<span data-ttu-id="1bbae-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1bbae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bbae-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1bbae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bbae-128">입력</span><span class="sxs-lookup"><span data-stu-id="1bbae-128">INPUTS</span></span>

### <span data-ttu-id="1bbae-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1bbae-129">System.String</span></span>

### <span data-ttu-id="1bbae-130">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1bbae-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1bbae-131">출력</span><span class="sxs-lookup"><span data-stu-id="1bbae-131">OUTPUTS</span></span>

### <span data-ttu-id="1bbae-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1bbae-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1bbae-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1bbae-133">NOTES</span></span>

## <span data-ttu-id="1bbae-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bbae-134">RELATED LINKS</span></span>

[<span data-ttu-id="1bbae-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1bbae-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="1bbae-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1bbae-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="1bbae-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1bbae-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="1bbae-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1bbae-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333753"
---
# <span data-ttu-id="66826-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="66826-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="66826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66826-102">SYNOPSIS</span></span>
<span data-ttu-id="66826-103">Batch 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="66826-103">Updates a Batch account.</span></span>

## <span data-ttu-id="66826-104">구문</span><span class="sxs-lookup"><span data-stu-id="66826-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66826-105">설명</span><span class="sxs-lookup"><span data-stu-id="66826-105">DESCRIPTION</span></span>
<span data-ttu-id="66826-106">**Set-AzBatchAccount** cmdlet은 Azure Batch 계정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="66826-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="66826-107">현재 이 cmdlet은 태그만 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66826-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="66826-108">예제</span><span class="sxs-lookup"><span data-stu-id="66826-108">EXAMPLES</span></span>

### <span data-ttu-id="66826-109">예제 1: Batch 계정의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="66826-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="66826-110">이 명령은 pfuller라는 계정의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="66826-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="66826-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66826-111">PARAMETERS</span></span>

### <span data-ttu-id="66826-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66826-112">-AccountName</span></span>
<span data-ttu-id="66826-113">이 cmdlet이 업데이트하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66826-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="66826-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="66826-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="66826-115">자동 저장소에 사용할 저장소 계정의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66826-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66826-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66826-116">-DefaultProfile</span></span>
<span data-ttu-id="66826-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66826-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66826-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66826-118">-ResourceGroupName</span></span>
<span data-ttu-id="66826-119">이 cmdlet이 업데이트하는 계정의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66826-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66826-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="66826-120">-Tag</span></span>
<span data-ttu-id="66826-121">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="66826-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="66826-122">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="66826-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66826-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66826-123">CommonParameters</span></span>
<span data-ttu-id="66826-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66826-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66826-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="66826-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66826-126">입력</span><span class="sxs-lookup"><span data-stu-id="66826-126">INPUTS</span></span>

### <span data-ttu-id="66826-127">System.String</span><span class="sxs-lookup"><span data-stu-id="66826-127">System.String</span></span>

### <span data-ttu-id="66826-128">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="66826-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="66826-129">출력</span><span class="sxs-lookup"><span data-stu-id="66826-129">OUTPUTS</span></span>

### <span data-ttu-id="66826-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="66826-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="66826-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66826-131">NOTES</span></span>

## <span data-ttu-id="66826-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66826-132">RELATED LINKS</span></span>

[<span data-ttu-id="66826-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="66826-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="66826-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="66826-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="66826-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="66826-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="66826-136">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="66826-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

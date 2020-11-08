---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219109"
---
# <span data-ttu-id="0c8f6-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0c8f6-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="0c8f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8f6-103">일괄 처리 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-103">Updates a Batch account.</span></span>

## <span data-ttu-id="0c8f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c8f6-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c8f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="0c8f6-106">**Set-AzBatchAccount** Cmdlet은 Azure Batch 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="0c8f6-107">현재이 cmdlet은 태그만 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="0c8f6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0c8f6-108">EXAMPLES</span></span>

### <span data-ttu-id="0c8f6-109">예제 1: 일괄 처리 계정의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="0c8f6-109">Example 1: Update the tags on a Batch account</span></span>
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

<span data-ttu-id="0c8f6-110">이 명령은 pfuller 계정에서 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="0c8f6-111">변수</span><span class="sxs-lookup"><span data-stu-id="0c8f6-111">PARAMETERS</span></span>

### <span data-ttu-id="0c8f6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c8f6-112">-AccountName</span></span>
<span data-ttu-id="0c8f6-113">이 cmdlet이 업데이트 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="0c8f6-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0c8f6-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="0c8f6-115">자동 저장소에 사용 되는 저장소 계정의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="0c8f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8f6-116">-DefaultProfile</span></span>
<span data-ttu-id="0c8f6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c8f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c8f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="0c8f6-119">이 cmdlet이 업데이트 하는 계정의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="0c8f6-120">태그</span><span class="sxs-lookup"><span data-stu-id="0c8f6-120">-Tag</span></span>
<span data-ttu-id="0c8f6-121">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0c8f6-122">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0c8f6-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0c8f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8f6-123">CommonParameters</span></span>
<span data-ttu-id="0c8f6-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8f6-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c8f6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8f6-126">입력</span><span class="sxs-lookup"><span data-stu-id="0c8f6-126">INPUTS</span></span>

### <span data-ttu-id="0c8f6-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c8f6-127">System.String</span></span>

### <span data-ttu-id="0c8f6-128">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="0c8f6-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0c8f6-129">출력</span><span class="sxs-lookup"><span data-stu-id="0c8f6-129">OUTPUTS</span></span>

### <span data-ttu-id="0c8f6-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0c8f6-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0c8f6-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0c8f6-131">NOTES</span></span>

## <span data-ttu-id="0c8f6-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c8f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c8f6-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0c8f6-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="0c8f6-134">새로운 AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0c8f6-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="0c8f6-135">제거-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0c8f6-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="0c8f6-136">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0c8f6-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

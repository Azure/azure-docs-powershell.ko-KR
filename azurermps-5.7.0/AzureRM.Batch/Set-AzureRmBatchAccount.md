---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: 7f1747d838d0b81d1cfa29e98134897357f33a53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527083"
---
# <span data-ttu-id="a5209-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a5209-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="a5209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5209-102">SYNOPSIS</span></span>
<span data-ttu-id="a5209-103">일괄 처리 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5209-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5209-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5209-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5209-105">DESCRIPTION</span></span>
<span data-ttu-id="a5209-106">**Set-AzureRmBatchAccount** Cmdlet은 Azure Batch 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="a5209-107">현재이 cmdlet은 태그만 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="a5209-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a5209-108">EXAMPLES</span></span>

### <span data-ttu-id="a5209-109">예제 1: 일괄 처리 계정의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="a5209-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
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

<span data-ttu-id="a5209-110">이 명령은 pfuller 계정에서 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="a5209-111">변수</span><span class="sxs-lookup"><span data-stu-id="a5209-111">PARAMETERS</span></span>

### <span data-ttu-id="a5209-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5209-112">-AccountName</span></span>
<span data-ttu-id="a5209-113">이 cmdlet이 업데이트 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a5209-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a5209-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="a5209-115">자동 저장소에 사용 되는 저장소 계정의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="a5209-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5209-116">-DefaultProfile</span></span>
<span data-ttu-id="a5209-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5209-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5209-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5209-119">이 cmdlet이 업데이트 하는 계정의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a5209-120">태그</span><span class="sxs-lookup"><span data-stu-id="a5209-120">-Tag</span></span>
<span data-ttu-id="a5209-121">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a5209-122">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a5209-122">For example:</span></span>

<span data-ttu-id="a5209-123">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a5209-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5209-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5209-124">CommonParameters</span></span>
<span data-ttu-id="a5209-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5209-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5209-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5209-127">입력</span><span class="sxs-lookup"><span data-stu-id="a5209-127">INPUTS</span></span>

### <span data-ttu-id="a5209-128">않아야</span><span class="sxs-lookup"><span data-stu-id="a5209-128">None</span></span>
<span data-ttu-id="a5209-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5209-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5209-130">출력</span><span class="sxs-lookup"><span data-stu-id="a5209-130">OUTPUTS</span></span>

### <span data-ttu-id="a5209-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a5209-131">BatchAccountContext</span></span>

## <span data-ttu-id="a5209-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a5209-132">NOTES</span></span>

## <span data-ttu-id="a5209-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5209-133">RELATED LINKS</span></span>

[<span data-ttu-id="a5209-134">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a5209-134">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="a5209-135">새로운 AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a5209-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="a5209-136">제거-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a5209-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="a5209-137">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a5209-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

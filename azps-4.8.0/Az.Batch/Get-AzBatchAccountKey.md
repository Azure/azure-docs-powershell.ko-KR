---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 2662eeeeaedbac75f443bf6160c625dfdb8dd854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056790"
---
# <span data-ttu-id="8ec26-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8ec26-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="8ec26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec26-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec26-103">일괄 처리 계정의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ec26-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="8ec26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ec26-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ec26-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec26-106">**AzBatchAccountKey** cmdlet은 현재 구독에서 Azure Batch 계정의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ec26-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="8ec26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ec26-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec26-108">예제 1: 일괄 계정 키를 가져오고 나중에 사용할 수 있도록 $Context 변수에 저장</span><span class="sxs-lookup"><span data-stu-id="8ec26-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="8ec26-109">이 명령은 계정 세부 정보를 가져와 `$Context` 나중에 사용할 수 있도록 개체에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec26-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="8ec26-110">예제 2: 일괄 처리 계정 키 가져오기 및 표시</span><span class="sxs-lookup"><span data-stu-id="8ec26-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="8ec26-111">이 명령은 계정 키를 가져와 콘솔에 인쇄 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec26-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="8ec26-112">변수</span><span class="sxs-lookup"><span data-stu-id="8ec26-112">PARAMETERS</span></span>

### <span data-ttu-id="8ec26-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ec26-113">-AccountName</span></span>
<span data-ttu-id="8ec26-114">이 cmdlet에서 키를 가져오는 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec26-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="8ec26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec26-115">-DefaultProfile</span></span>
<span data-ttu-id="8ec26-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ec26-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec26-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ec26-118">이 cmdlet에서 키를 가져오는 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec26-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="8ec26-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec26-119">CommonParameters</span></span>
<span data-ttu-id="8ec26-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ec26-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec26-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8ec26-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec26-122">입력</span><span class="sxs-lookup"><span data-stu-id="8ec26-122">INPUTS</span></span>

### <span data-ttu-id="8ec26-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ec26-123">System.String</span></span>

## <span data-ttu-id="8ec26-124">출력</span><span class="sxs-lookup"><span data-stu-id="8ec26-124">OUTPUTS</span></span>

### <span data-ttu-id="8ec26-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8ec26-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8ec26-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8ec26-126">NOTES</span></span>

## <span data-ttu-id="8ec26-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ec26-127">RELATED LINKS</span></span>

[<span data-ttu-id="8ec26-128">새로운 AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8ec26-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="8ec26-129">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ec26-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

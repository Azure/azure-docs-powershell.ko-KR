---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 07671d3318e599c9b63c4981df1ceac63178bb35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001883"
---
# <span data-ttu-id="b907d-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b907d-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="b907d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b907d-102">SYNOPSIS</span></span>
<span data-ttu-id="b907d-103">Batch 계정의 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="b907d-104">구문</span><span class="sxs-lookup"><span data-stu-id="b907d-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b907d-105">설명</span><span class="sxs-lookup"><span data-stu-id="b907d-105">DESCRIPTION</span></span>
<span data-ttu-id="b907d-106">**Get-AzBatchAccountKey** cmdlet은 현재 구독에서 Azure Batch 계정의 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="b907d-107">예제</span><span class="sxs-lookup"><span data-stu-id="b907d-107">EXAMPLES</span></span>

### <span data-ttu-id="b907d-108">예제 1: 일괄 처리 계정 키를 구하고 나중에 사용할 $Context 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="b907d-109">이 명령은 계정 세부 정보를 얻게 하여 나중에 사용할 `$Context` 개체에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="b907d-110">예제 2: 일괄 처리 계정 키 및 표시</span><span class="sxs-lookup"><span data-stu-id="b907d-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="b907d-111">이 명령은 계정 키를 얻게 하여 콘솔에 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="b907d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b907d-112">PARAMETERS</span></span>

### <span data-ttu-id="b907d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b907d-113">-AccountName</span></span>
<span data-ttu-id="b907d-114">이 cmdlet에서 키를 받을 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="b907d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b907d-115">-DefaultProfile</span></span>
<span data-ttu-id="b907d-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b907d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b907d-117">-ResourceGroupName</span></span>
<span data-ttu-id="b907d-118">이 cmdlet에서 키를 얻을 수 있는 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="b907d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b907d-119">CommonParameters</span></span>
<span data-ttu-id="b907d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b907d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b907d-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b907d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b907d-122">입력</span><span class="sxs-lookup"><span data-stu-id="b907d-122">INPUTS</span></span>

### <span data-ttu-id="b907d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b907d-123">System.String</span></span>

## <span data-ttu-id="b907d-124">출력</span><span class="sxs-lookup"><span data-stu-id="b907d-124">OUTPUTS</span></span>

### <span data-ttu-id="b907d-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b907d-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b907d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b907d-126">NOTES</span></span>

## <span data-ttu-id="b907d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b907d-127">RELATED LINKS</span></span>

[<span data-ttu-id="b907d-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b907d-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="b907d-129">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b907d-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 2662eeeeaedbac75f443bf6160c625dfdb8dd854
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199545"
---
# <span data-ttu-id="40db2-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="40db2-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="40db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40db2-102">SYNOPSIS</span></span>
<span data-ttu-id="40db2-103">Batch 계정의 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40db2-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="40db2-104">구문</span><span class="sxs-lookup"><span data-stu-id="40db2-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40db2-105">설명</span><span class="sxs-lookup"><span data-stu-id="40db2-105">DESCRIPTION</span></span>
<span data-ttu-id="40db2-106">**Get-AzBatchAccountKey** cmdlet은 현재 구독에서 Azure Batch 계정의 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40db2-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="40db2-107">예제</span><span class="sxs-lookup"><span data-stu-id="40db2-107">EXAMPLES</span></span>

### <span data-ttu-id="40db2-108">예제 1: 일괄 처리 계정 키를 사용하여 나중에 사용할 $Context 변수에 저장</span><span class="sxs-lookup"><span data-stu-id="40db2-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="40db2-109">이 명령은 계정 세부 정보를 얻게 하여 나중에 사용할 수 `$Context` 있는 개체에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="40db2-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="40db2-110">예제 2: 일괄 처리 계정 키 및 표시</span><span class="sxs-lookup"><span data-stu-id="40db2-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="40db2-111">이 명령은 계정 키를 얻게 하여 콘솔에 인쇄합니다.</span><span class="sxs-lookup"><span data-stu-id="40db2-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="40db2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40db2-112">PARAMETERS</span></span>

### <span data-ttu-id="40db2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40db2-113">-AccountName</span></span>
<span data-ttu-id="40db2-114">이 cmdlet에서 키를 얻을 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40db2-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="40db2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40db2-115">-DefaultProfile</span></span>
<span data-ttu-id="40db2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40db2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40db2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40db2-117">-ResourceGroupName</span></span>
<span data-ttu-id="40db2-118">이 cmdlet에서 키를 얻을 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="40db2-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="40db2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40db2-119">CommonParameters</span></span>
<span data-ttu-id="40db2-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40db2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40db2-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40db2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40db2-122">입력</span><span class="sxs-lookup"><span data-stu-id="40db2-122">INPUTS</span></span>

### <span data-ttu-id="40db2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="40db2-123">System.String</span></span>

## <span data-ttu-id="40db2-124">출력</span><span class="sxs-lookup"><span data-stu-id="40db2-124">OUTPUTS</span></span>

### <span data-ttu-id="40db2-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="40db2-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="40db2-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40db2-126">NOTES</span></span>

## <span data-ttu-id="40db2-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40db2-127">RELATED LINKS</span></span>

[<span data-ttu-id="40db2-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="40db2-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="40db2-129">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="40db2-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

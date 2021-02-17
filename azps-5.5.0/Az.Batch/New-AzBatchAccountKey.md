---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205216"
---
# <span data-ttu-id="3cf11-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3cf11-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="3cf11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf11-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf11-103">Batch 계정의 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf11-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="3cf11-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cf11-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cf11-105">설명</span><span class="sxs-lookup"><span data-stu-id="3cf11-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf11-106">**New-AzBatchAccountKey** cmdlet은 Azure Batch 계정의 기본 또는 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf11-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="3cf11-107">cmdlet은 현재 **PrimaryAccountKey** 및 **SecondaryAccountKey 속성이 있는 BatchAccountContext 개체를 반환합니다.** </span><span class="sxs-lookup"><span data-stu-id="3cf11-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="3cf11-108">예제</span><span class="sxs-lookup"><span data-stu-id="3cf11-108">EXAMPLES</span></span>

### <span data-ttu-id="3cf11-109">예제 1: Batch 계정에서 기본 계정 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="3cf11-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="3cf11-110">이 명령은 pfuller라는 Batch 계정의 기본 계정 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf11-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="3cf11-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cf11-111">PARAMETERS</span></span>

### <span data-ttu-id="3cf11-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3cf11-112">-AccountName</span></span>
<span data-ttu-id="3cf11-113">이 cmdlet이 키를 다시 생성하는 Batch 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf11-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="3cf11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf11-114">-DefaultProfile</span></span>
<span data-ttu-id="3cf11-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cf11-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cf11-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3cf11-116">-KeyType</span></span>
<span data-ttu-id="3cf11-117">이 cmdlet이 다시 생성하는 키의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf11-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="3cf11-118">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="3cf11-118">Valid values are:</span></span>
- <span data-ttu-id="3cf11-119">기본</span><span class="sxs-lookup"><span data-stu-id="3cf11-119">Primary</span></span>
- <span data-ttu-id="3cf11-120">보조</span><span class="sxs-lookup"><span data-stu-id="3cf11-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf11-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf11-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cf11-122">이 cmdlet이 키를 다시 생성하는 계정의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf11-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="3cf11-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf11-123">CommonParameters</span></span>
<span data-ttu-id="3cf11-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cf11-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf11-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cf11-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf11-126">입력</span><span class="sxs-lookup"><span data-stu-id="3cf11-126">INPUTS</span></span>

### <span data-ttu-id="3cf11-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3cf11-127">System.String</span></span>

## <span data-ttu-id="3cf11-128">출력</span><span class="sxs-lookup"><span data-stu-id="3cf11-128">OUTPUTS</span></span>

### <span data-ttu-id="3cf11-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3cf11-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3cf11-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cf11-130">NOTES</span></span>

## <span data-ttu-id="3cf11-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cf11-131">RELATED LINKS</span></span>

[<span data-ttu-id="3cf11-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3cf11-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3cf11-133">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3cf11-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

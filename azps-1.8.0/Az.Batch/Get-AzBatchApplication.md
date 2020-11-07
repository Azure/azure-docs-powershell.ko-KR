---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: fa08214e141d035e7c449e591f6a4820f758b48c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701473"
---
# <span data-ttu-id="c2c4d-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c2c4d-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="c2c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c4d-103">지정 된 응용 프로그램에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="c2c4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2c4d-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2c4d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c2c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="c2c4d-106">**AzBatchApplication** Cmdlet은 Azure Batch 계정에서 응용 프로그램에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="c2c4d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c2c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="c2c4d-108">예제 1: 일괄 처리 계정에 응용 프로그램 표시</span><span class="sxs-lookup"><span data-stu-id="c2c4d-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="c2c4d-109">이 명령은 ContosoBatch account의 모든 응용 프로그램을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="c2c4d-110">변수</span><span class="sxs-lookup"><span data-stu-id="c2c4d-110">PARAMETERS</span></span>

### <span data-ttu-id="c2c4d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2c4d-111">-AccountName</span></span>
<span data-ttu-id="c2c4d-112">응용 프로그램을 포함 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-112">Specifies the name of the Batch account that contains the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c4d-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c2c4d-113">-ApplicationId</span></span>
<span data-ttu-id="c2c4d-114">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c4d-115">-DefaultProfile</span></span>
<span data-ttu-id="c2c4d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2c4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2c4d-118">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c4d-119">CommonParameters</span></span>
<span data-ttu-id="c2c4d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c4d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c4d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c4d-122">입력</span><span class="sxs-lookup"><span data-stu-id="c2c4d-122">INPUTS</span></span>

### <span data-ttu-id="c2c4d-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2c4d-123">System.String</span></span>

## <span data-ttu-id="c2c4d-124">출력</span><span class="sxs-lookup"><span data-stu-id="c2c4d-124">OUTPUTS</span></span>

### <span data-ttu-id="c2c4d-125">Microsoft.Azure.Commands.Batch. PSApplication 모델</span><span class="sxs-lookup"><span data-stu-id="c2c4d-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="c2c4d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="c2c4d-126">NOTES</span></span>

## <span data-ttu-id="c2c4d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2c4d-127">RELATED LINKS</span></span>

[<span data-ttu-id="c2c4d-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c2c4d-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="c2c4d-129">새로운 AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c2c4d-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="c2c4d-130">새로운 AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c2c4d-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="c2c4d-131">제거-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c2c4d-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="c2c4d-132">제거-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c2c4d-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="c2c4d-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c2c4d-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



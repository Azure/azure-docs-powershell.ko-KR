---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: e22d3c58072fbabd3f927f6b9065f22422492622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525348"
---
# <span data-ttu-id="38404-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="38404-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="38404-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38404-102">SYNOPSIS</span></span>
<span data-ttu-id="38404-103">지정 된 응용 프로그램에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="38404-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38404-104">구문과</span><span class="sxs-lookup"><span data-stu-id="38404-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38404-105">설명은</span><span class="sxs-lookup"><span data-stu-id="38404-105">DESCRIPTION</span></span>
<span data-ttu-id="38404-106">**AzureRmBatchApplication** Cmdlet은 Azure Batch 계정에서 응용 프로그램에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="38404-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="38404-107">예제의</span><span class="sxs-lookup"><span data-stu-id="38404-107">EXAMPLES</span></span>

### <span data-ttu-id="38404-108">예제 1: 일괄 처리 계정에 응용 프로그램 표시</span><span class="sxs-lookup"><span data-stu-id="38404-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="38404-109">이 명령은 ContosoBatch account의 모든 응용 프로그램을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="38404-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="38404-110">변수</span><span class="sxs-lookup"><span data-stu-id="38404-110">PARAMETERS</span></span>

### <span data-ttu-id="38404-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="38404-111">-AccountName</span></span>
<span data-ttu-id="38404-112">응용 프로그램을 포함 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38404-112">Specifies the name of the Batch account that contains the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38404-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="38404-113">-ApplicationId</span></span>
<span data-ttu-id="38404-114">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38404-114">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38404-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38404-115">-DefaultProfile</span></span>
<span data-ttu-id="38404-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38404-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38404-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38404-117">-ResourceGroupName</span></span>
<span data-ttu-id="38404-118">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38404-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38404-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38404-119">CommonParameters</span></span>
<span data-ttu-id="38404-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38404-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38404-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38404-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38404-122">입력</span><span class="sxs-lookup"><span data-stu-id="38404-122">INPUTS</span></span>

### <span data-ttu-id="38404-123">않아야</span><span class="sxs-lookup"><span data-stu-id="38404-123">None</span></span>
<span data-ttu-id="38404-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38404-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38404-125">출력</span><span class="sxs-lookup"><span data-stu-id="38404-125">OUTPUTS</span></span>

### <span data-ttu-id="38404-126">Microsoft.Azure.Commands.Batch. PSApplication 모델</span><span class="sxs-lookup"><span data-stu-id="38404-126">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="38404-127">상속자</span><span class="sxs-lookup"><span data-stu-id="38404-127">NOTES</span></span>

## <span data-ttu-id="38404-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38404-128">RELATED LINKS</span></span>

[<span data-ttu-id="38404-129">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="38404-129">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="38404-130">새로운 AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="38404-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="38404-131">새로운 AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="38404-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="38404-132">제거-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="38404-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="38404-133">제거-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="38404-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="38404-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="38404-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)



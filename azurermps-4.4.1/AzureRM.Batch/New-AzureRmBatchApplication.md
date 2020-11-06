---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 6c2ab80f5b9fb38ed2f6399d9f186134f4659edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531846"
---
# <span data-ttu-id="66e35-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="66e35-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="66e35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66e35-102">SYNOPSIS</span></span>
<span data-ttu-id="66e35-103">지정 된 Batch 계정에 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66e35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66e35-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66e35-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66e35-105">DESCRIPTION</span></span>
<span data-ttu-id="66e35-106">**새 AzureRmBatchApplication** cmdlet은 지정 된 Azure Batch 계정에 응용 프로그램을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="66e35-107">예제의</span><span class="sxs-lookup"><span data-stu-id="66e35-107">EXAMPLES</span></span>

### <span data-ttu-id="66e35-108">예제 1: 일괄 처리 계정에 빈 응용 프로그램 추가</span><span class="sxs-lookup"><span data-stu-id="66e35-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="66e35-109">이 명령은 ContosoBatch 계정에 Litware 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="66e35-110">응용 프로그램에는 처음에 패키지가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="66e35-111">변수</span><span class="sxs-lookup"><span data-stu-id="66e35-111">PARAMETERS</span></span>

### <span data-ttu-id="66e35-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66e35-112">-AccountName</span></span>
<span data-ttu-id="66e35-113">이 cmdlet이 응용 프로그램을 추가 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="66e35-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="66e35-114">-AllowUpdates</span></span>
<span data-ttu-id="66e35-115">동일한 버전 문자열을 사용 하 여 응용 프로그램 내에서 패키지를 덮어쓸 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e35-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="66e35-116">-ApplicationId</span></span>
<span data-ttu-id="66e35-117">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-117">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e35-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="66e35-118">-DisplayName</span></span>
<span data-ttu-id="66e35-119">응용 프로그램의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-119">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e35-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e35-120">-ResourceGroupName</span></span>
<span data-ttu-id="66e35-121">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="66e35-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e35-122">-DefaultProfile</span></span>
<span data-ttu-id="66e35-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e35-124">CommonParameters</span></span>
<span data-ttu-id="66e35-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66e35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e35-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66e35-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e35-127">입력</span><span class="sxs-lookup"><span data-stu-id="66e35-127">INPUTS</span></span>

## <span data-ttu-id="66e35-128">출력</span><span class="sxs-lookup"><span data-stu-id="66e35-128">OUTPUTS</span></span>

### <span data-ttu-id="66e35-129">Microsoft.Azure.Commands.Batch. PSApplication 모델</span><span class="sxs-lookup"><span data-stu-id="66e35-129">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="66e35-130">상속자</span><span class="sxs-lookup"><span data-stu-id="66e35-130">NOTES</span></span>

## <span data-ttu-id="66e35-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66e35-131">RELATED LINKS</span></span>

[<span data-ttu-id="66e35-132">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="66e35-132">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="66e35-133">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="66e35-133">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="66e35-134">새로운 AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="66e35-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="66e35-135">제거-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="66e35-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="66e35-136">제거-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="66e35-136">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="66e35-137">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="66e35-137">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)



---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: b8169b2f05b4272c92989768e672b30aee105f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535000"
---
# <span data-ttu-id="54aae-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54aae-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="54aae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54aae-102">SYNOPSIS</span></span>
<span data-ttu-id="54aae-103">지정 된 응용 프로그램에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54aae-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54aae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54aae-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54aae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54aae-105">DESCRIPTION</span></span>
<span data-ttu-id="54aae-106">**AzureRmBatchApplication** Cmdlet은 Azure Batch 계정에서 응용 프로그램에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="54aae-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="54aae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54aae-107">EXAMPLES</span></span>

### <span data-ttu-id="54aae-108">예제 1: 일괄 처리 계정에 응용 프로그램 표시</span><span class="sxs-lookup"><span data-stu-id="54aae-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="54aae-109">이 명령은 ContosoBatch account의 모든 응용 프로그램을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54aae-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="54aae-110">변수</span><span class="sxs-lookup"><span data-stu-id="54aae-110">PARAMETERS</span></span>

### <span data-ttu-id="54aae-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54aae-111">-AccountName</span></span>
<span data-ttu-id="54aae-112">응용 프로그램을 포함 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54aae-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="54aae-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="54aae-113">-ApplicationId</span></span>
<span data-ttu-id="54aae-114">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54aae-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="54aae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54aae-115">-ResourceGroupName</span></span>
<span data-ttu-id="54aae-116">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54aae-116">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="54aae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54aae-117">-DefaultProfile</span></span>
<span data-ttu-id="54aae-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54aae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54aae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54aae-119">CommonParameters</span></span>
<span data-ttu-id="54aae-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54aae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54aae-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54aae-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54aae-122">입력</span><span class="sxs-lookup"><span data-stu-id="54aae-122">INPUTS</span></span>

## <span data-ttu-id="54aae-123">출력</span><span class="sxs-lookup"><span data-stu-id="54aae-123">OUTPUTS</span></span>

### <span data-ttu-id="54aae-124">Microsoft.Azure.Commands.Batch. PSApplication 모델</span><span class="sxs-lookup"><span data-stu-id="54aae-124">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="54aae-125">상속자</span><span class="sxs-lookup"><span data-stu-id="54aae-125">NOTES</span></span>

## <span data-ttu-id="54aae-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54aae-126">RELATED LINKS</span></span>

[<span data-ttu-id="54aae-127">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54aae-127">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="54aae-128">새로운 AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54aae-128">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="54aae-129">새로운 AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54aae-129">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="54aae-130">제거-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54aae-130">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="54aae-131">제거-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="54aae-131">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="54aae-132">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="54aae-132">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)



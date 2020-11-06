---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: 61288340bb2b9acb2bd47388d8f776d5c732b6f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526292"
---
# <span data-ttu-id="1cfed-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1cfed-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="1cfed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cfed-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfed-103">일괄 처리 계정에서 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cfed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1cfed-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cfed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1cfed-105">DESCRIPTION</span></span>
<span data-ttu-id="1cfed-106">**AzureRmBatchApplication** Cmdlet은 Azure Batch 계정에서 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="1cfed-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1cfed-107">EXAMPLES</span></span>

### <span data-ttu-id="1cfed-108">예제 1: 일괄 처리 계정에서 응용 프로그램 삭제</span><span class="sxs-lookup"><span data-stu-id="1cfed-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="1cfed-109">이 명령은 ContosoBatch 계정에서 Litware 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="1cfed-110">응용 프로그램에 패키지가 포함 되어 있으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="1cfed-111">변수</span><span class="sxs-lookup"><span data-stu-id="1cfed-111">PARAMETERS</span></span>

### <span data-ttu-id="1cfed-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1cfed-112">-AccountName</span></span>
<span data-ttu-id="1cfed-113">이 cmdlet이 응용 프로그램을 제거 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="1cfed-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1cfed-114">-ApplicationId</span></span>
<span data-ttu-id="1cfed-115">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="1cfed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfed-116">-DefaultProfile</span></span>
<span data-ttu-id="1cfed-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cfed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cfed-118">-ResourceGroupName</span></span>
<span data-ttu-id="1cfed-119">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="1cfed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfed-120">CommonParameters</span></span>
<span data-ttu-id="1cfed-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cfed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfed-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cfed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfed-123">입력</span><span class="sxs-lookup"><span data-stu-id="1cfed-123">INPUTS</span></span>

### <span data-ttu-id="1cfed-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1cfed-124">System.String</span></span>

## <span data-ttu-id="1cfed-125">출력</span><span class="sxs-lookup"><span data-stu-id="1cfed-125">OUTPUTS</span></span>

### <span data-ttu-id="1cfed-126">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="1cfed-126">System.Void</span></span>

## <span data-ttu-id="1cfed-127">상속자</span><span class="sxs-lookup"><span data-stu-id="1cfed-127">NOTES</span></span>

## <span data-ttu-id="1cfed-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cfed-128">RELATED LINKS</span></span>

[<span data-ttu-id="1cfed-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1cfed-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="1cfed-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1cfed-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1cfed-131">새로운 AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1cfed-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="1cfed-132">새로운 AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1cfed-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1cfed-133">제거-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1cfed-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="1cfed-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1cfed-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)



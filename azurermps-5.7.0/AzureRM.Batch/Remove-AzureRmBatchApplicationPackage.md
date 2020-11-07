---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 0ae0003c4c38b7e3922694ed01f6d8f4d10a49d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711442"
---
# <span data-ttu-id="c9d9a-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c9d9a-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="c9d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d9a-103">응용 프로그램 패키지 레코드와 이진 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9d9a-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9d9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d9a-106">**AzureRmBatchApplicationPackage** cmdlet은 앱 패키지 레코드와 Azure Batch 계정에서 바이너리 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="c9d9a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c9d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d9a-108">예제 1: 일괄 처리 계정에서 응용 프로그램 패키지 삭제</span><span class="sxs-lookup"><span data-stu-id="c9d9a-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="c9d9a-109">이 명령은 ContosoBatchGroup 계정에서 Litware 응용 프로그램의 버전 1.0을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="c9d9a-110">이 명령은 패키지 레코드와 패키지 이진 파일을 포함 하는 blob을 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="c9d9a-111">변수</span><span class="sxs-lookup"><span data-stu-id="c9d9a-111">PARAMETERS</span></span>

### <span data-ttu-id="c9d9a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c9d9a-112">-AccountName</span></span>
<span data-ttu-id="c9d9a-113">이 cmdlet이 응용 프로그램 패키지를 삭제 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="c9d9a-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c9d9a-114">-ApplicationId</span></span>
<span data-ttu-id="c9d9a-115">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-115">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d9a-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="c9d9a-116">-ApplicationVersion</span></span>
<span data-ttu-id="c9d9a-117">응용 프로그램의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-117">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d9a-118">-DefaultProfile</span></span>
<span data-ttu-id="c9d9a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d9a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d9a-120">-ResourceGroupName</span></span>
<span data-ttu-id="c9d9a-121">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="c9d9a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d9a-122">CommonParameters</span></span>
<span data-ttu-id="c9d9a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d9a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d9a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d9a-125">입력</span><span class="sxs-lookup"><span data-stu-id="c9d9a-125">INPUTS</span></span>

### <span data-ttu-id="c9d9a-126">않아야</span><span class="sxs-lookup"><span data-stu-id="c9d9a-126">None</span></span>
<span data-ttu-id="c9d9a-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9d9a-128">출력</span><span class="sxs-lookup"><span data-stu-id="c9d9a-128">OUTPUTS</span></span>

## <span data-ttu-id="c9d9a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c9d9a-129">NOTES</span></span>

## <span data-ttu-id="c9d9a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9d9a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9d9a-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c9d9a-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="c9d9a-132">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c9d9a-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c9d9a-133">새로운 AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c9d9a-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="c9d9a-134">새로운 AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c9d9a-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c9d9a-135">제거-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c9d9a-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="c9d9a-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c9d9a-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)



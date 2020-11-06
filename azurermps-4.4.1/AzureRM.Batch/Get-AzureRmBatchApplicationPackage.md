---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: f260af1bc26d9cf921a26e4f08c3c4feab4b79c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530805"
---
# <span data-ttu-id="8e6e6-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8e6e6-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="8e6e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6e6-103">일괄 계정에서 응용 프로그램 패키지에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e6e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e6e6-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e6e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e6e6-105">DESCRIPTION</span></span>
<span data-ttu-id="8e6e6-106">**AzureRmBatchApplicationPackage** Cmdlet은 Azure Batch 계정에서 응용 프로그램 패키지에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="8e6e6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e6e6-107">EXAMPLES</span></span>

### <span data-ttu-id="8e6e6-108">예제 1: 일괄 처리 계정에서 응용 프로그램 패키지에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8e6e6-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="8e6e6-109">이 명령은 Litware 패키지의 버전 1.0에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="8e6e6-110">변수</span><span class="sxs-lookup"><span data-stu-id="8e6e6-110">PARAMETERS</span></span>

### <span data-ttu-id="8e6e6-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e6e6-111">-AccountName</span></span>
<span data-ttu-id="8e6e6-112">이 cmdlet에서 정보를 가져오는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="8e6e6-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8e6e6-113">-ApplicationId</span></span>
<span data-ttu-id="8e6e6-114">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="8e6e6-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="8e6e6-115">-ApplicationVersion</span></span>
<span data-ttu-id="8e6e6-116">응용 프로그램의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e6e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e6e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e6e6-118">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="8e6e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e6e6-119">-DefaultProfile</span></span>
<span data-ttu-id="8e6e6-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e6e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6e6-121">CommonParameters</span></span>
<span data-ttu-id="8e6e6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e6e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6e6-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e6e6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6e6-124">입력</span><span class="sxs-lookup"><span data-stu-id="8e6e6-124">INPUTS</span></span>

## <span data-ttu-id="8e6e6-125">출력</span><span class="sxs-lookup"><span data-stu-id="8e6e6-125">OUTPUTS</span></span>

### <span data-ttu-id="8e6e6-126">Microsoft.Azure.Commands.Batch. PSApplicationPackage 모델</span><span class="sxs-lookup"><span data-stu-id="8e6e6-126">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="8e6e6-127">상속자</span><span class="sxs-lookup"><span data-stu-id="8e6e6-127">NOTES</span></span>

## <span data-ttu-id="8e6e6-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e6e6-128">RELATED LINKS</span></span>

[<span data-ttu-id="8e6e6-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8e6e6-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="8e6e6-130">새로운 AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8e6e6-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="8e6e6-131">새로운 AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8e6e6-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="8e6e6-132">제거-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8e6e6-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="8e6e6-133">제거-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8e6e6-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="8e6e6-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8e6e6-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)



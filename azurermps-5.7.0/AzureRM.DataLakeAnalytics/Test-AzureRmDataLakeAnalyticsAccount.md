---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a6e147d64a1dea77febc833b5c46e78d070f3ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526852"
---
# <span data-ttu-id="d6b56-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d6b56-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d6b56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b56-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b56-103">Data Lake Analytics 계정이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b56-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6b56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6b56-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6b56-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d6b56-105">DESCRIPTION</span></span>
<span data-ttu-id="d6b56-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet은 Data Lake Analytics 계정이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b56-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d6b56-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d6b56-107">EXAMPLES</span></span>

### <span data-ttu-id="d6b56-108">예제 1: 계정이 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="d6b56-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="d6b56-109">이 명령은 ContosoAdlAccount 이라는 계정이 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b56-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="d6b56-110">변수</span><span class="sxs-lookup"><span data-stu-id="d6b56-110">PARAMETERS</span></span>

### <span data-ttu-id="d6b56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b56-111">-DefaultProfile</span></span>
<span data-ttu-id="d6b56-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d6b56-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6b56-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d6b56-113">-Name</span></span>
<span data-ttu-id="d6b56-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b56-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d6b56-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b56-115">-ResourceGroupName</span></span>
<span data-ttu-id="d6b56-116">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b56-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b56-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b56-117">CommonParameters</span></span>
<span data-ttu-id="d6b56-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b56-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b56-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b56-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b56-120">입력</span><span class="sxs-lookup"><span data-stu-id="d6b56-120">INPUTS</span></span>

### <span data-ttu-id="d6b56-121">않아야</span><span class="sxs-lookup"><span data-stu-id="d6b56-121">None</span></span>
<span data-ttu-id="d6b56-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6b56-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6b56-123">출력</span><span class="sxs-lookup"><span data-stu-id="d6b56-123">OUTPUTS</span></span>

### <span data-ttu-id="d6b56-124">부울</span><span class="sxs-lookup"><span data-stu-id="d6b56-124">bool</span></span>
<span data-ttu-id="d6b56-125">계정이 있는지 여부를 나타내는 True 또는 false입니다.</span><span class="sxs-lookup"><span data-stu-id="d6b56-125">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="d6b56-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d6b56-126">NOTES</span></span>

## <span data-ttu-id="d6b56-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6b56-127">RELATED LINKS</span></span>

[<span data-ttu-id="d6b56-128">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d6b56-128">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d6b56-129">새로운 AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d6b56-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d6b56-130">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d6b56-130">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)



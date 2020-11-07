---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702380"
---
# <span data-ttu-id="7cfd5-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7cfd5-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="7cfd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cfd5-102">SYNOPSIS</span></span>
<span data-ttu-id="7cfd5-103">Data Lake Analytics 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cfd5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7cfd5-104">SYNTAX</span></span>

### <span data-ttu-id="7cfd5-105">GetAllInSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="7cfd5-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cfd5-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7cfd5-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cfd5-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="7cfd5-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cfd5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7cfd5-108">DESCRIPTION</span></span>
<span data-ttu-id="7cfd5-109">**AzureRmDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7cfd5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7cfd5-110">EXAMPLES</span></span>

### <span data-ttu-id="7cfd5-111">예제 1: Data Lake Analytics 계정에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7cfd5-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="7cfd5-112">이 명령은 ContosoAdlAccount 이라는 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="7cfd5-113">변수</span><span class="sxs-lookup"><span data-stu-id="7cfd5-113">PARAMETERS</span></span>

### <span data-ttu-id="7cfd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cfd5-114">-DefaultProfile</span></span>
<span data-ttu-id="7cfd5-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7cfd5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cfd5-116">-이름</span><span class="sxs-lookup"><span data-stu-id="7cfd5-116">-Name</span></span>
<span data-ttu-id="7cfd5-117">Data Lake Analytics 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cfd5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cfd5-118">-ResourceGroupName</span></span>
<span data-ttu-id="7cfd5-119">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cfd5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cfd5-120">CommonParameters</span></span>
<span data-ttu-id="7cfd5-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cfd5-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cfd5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cfd5-123">입력</span><span class="sxs-lookup"><span data-stu-id="7cfd5-123">INPUTS</span></span>

### <span data-ttu-id="7cfd5-124">않아야</span><span class="sxs-lookup"><span data-stu-id="7cfd5-124">None</span></span>
<span data-ttu-id="7cfd5-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7cfd5-126">출력</span><span class="sxs-lookup"><span data-stu-id="7cfd5-126">OUTPUTS</span></span>

### <span data-ttu-id="7cfd5-127">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7cfd5-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="7cfd5-128">지정 된 계정 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-128">The specified account details.</span></span>

### <span data-ttu-id="7cfd5-129">목록<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="7cfd5-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="7cfd5-130">지정 된 리소스 그룹 또는 구독의 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7cfd5-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="7cfd5-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7cfd5-131">NOTES</span></span>

## <span data-ttu-id="7cfd5-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cfd5-132">RELATED LINKS</span></span>

[<span data-ttu-id="7cfd5-133">새로운 AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7cfd5-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7cfd5-134">제거-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7cfd5-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7cfd5-135">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7cfd5-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="7cfd5-136">테스트-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="7cfd5-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)



---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702224"
---
# <span data-ttu-id="e93fa-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e93fa-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e93fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e93fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e93fa-103">Data Lake Analytics 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e93fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e93fa-104">SYNTAX</span></span>

### <span data-ttu-id="e93fa-105">모든 구독에서 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e93fa-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e93fa-106">모두 리소스 그룹에서</span><span class="sxs-lookup"><span data-stu-id="e93fa-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e93fa-107">특정 계정</span><span class="sxs-lookup"><span data-stu-id="e93fa-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e93fa-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e93fa-108">DESCRIPTION</span></span>
<span data-ttu-id="e93fa-109">**AzureRmDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e93fa-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e93fa-110">EXAMPLES</span></span>

### <span data-ttu-id="e93fa-111">예제 1: Data Lake Analytics 계정에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="e93fa-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="e93fa-112">이 명령은 ContosoAdlAccount 이라는 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="e93fa-113">변수</span><span class="sxs-lookup"><span data-stu-id="e93fa-113">PARAMETERS</span></span>

### <span data-ttu-id="e93fa-114">-이름</span><span class="sxs-lookup"><span data-stu-id="e93fa-114">-Name</span></span>
<span data-ttu-id="e93fa-115">Data Lake Analytics 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93fa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93fa-116">-ResourceGroupName</span></span>
<span data-ttu-id="e93fa-117">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93fa-118">-DefaultProfile</span></span>
<span data-ttu-id="e93fa-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93fa-120">CommonParameters</span></span>
<span data-ttu-id="e93fa-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93fa-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e93fa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93fa-123">입력</span><span class="sxs-lookup"><span data-stu-id="e93fa-123">INPUTS</span></span>

## <span data-ttu-id="e93fa-124">출력</span><span class="sxs-lookup"><span data-stu-id="e93fa-124">OUTPUTS</span></span>

### <span data-ttu-id="e93fa-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e93fa-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="e93fa-126">지정 된 계정 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-126">The specified account details.</span></span>

### <span data-ttu-id="e93fa-127">목록<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="e93fa-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="e93fa-128">지정 된 리소스 그룹 또는 구독의 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e93fa-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="e93fa-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e93fa-129">NOTES</span></span>

## <span data-ttu-id="e93fa-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e93fa-130">RELATED LINKS</span></span>

[<span data-ttu-id="e93fa-131">새로운 AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e93fa-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e93fa-132">제거-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e93fa-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e93fa-133">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e93fa-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e93fa-134">테스트-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e93fa-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b0390f4ec9ec7c141e7d059c88d7aeb4b9c8507d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696929"
---
# <span data-ttu-id="5f5cc-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5f5cc-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="5f5cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5cc-103">Data Lake Analytics 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f5cc-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="5f5cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f5cc-104">SYNTAX</span></span>

### <span data-ttu-id="5f5cc-105">GetAllInSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="5f5cc-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f5cc-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5f5cc-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f5cc-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="5f5cc-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f5cc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5f5cc-108">DESCRIPTION</span></span>
<span data-ttu-id="5f5cc-109">**AzDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f5cc-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5f5cc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5f5cc-110">EXAMPLES</span></span>

### <span data-ttu-id="5f5cc-111">예제 1: Data Lake Analytics 계정에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="5f5cc-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="5f5cc-112">이 명령은 ContosoAdlAccount 이라는 계정에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f5cc-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="5f5cc-113">변수</span><span class="sxs-lookup"><span data-stu-id="5f5cc-113">PARAMETERS</span></span>

### <span data-ttu-id="5f5cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5cc-114">-DefaultProfile</span></span>
<span data-ttu-id="5f5cc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5f5cc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f5cc-116">-이름</span><span class="sxs-lookup"><span data-stu-id="5f5cc-116">-Name</span></span>
<span data-ttu-id="5f5cc-117">Data Lake Analytics 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5cc-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f5cc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f5cc-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f5cc-119">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5cc-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f5cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5cc-120">CommonParameters</span></span>
<span data-ttu-id="5f5cc-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f5cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5cc-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5cc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5cc-123">입력</span><span class="sxs-lookup"><span data-stu-id="5f5cc-123">INPUTS</span></span>

### <span data-ttu-id="5f5cc-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5f5cc-124">System.String</span></span>

## <span data-ttu-id="5f5cc-125">출력</span><span class="sxs-lookup"><span data-stu-id="5f5cc-125">OUTPUTS</span></span>

### <span data-ttu-id="5f5cc-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5f5cc-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="5f5cc-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="5f5cc-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="5f5cc-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5f5cc-128">NOTES</span></span>

## <span data-ttu-id="5f5cc-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f5cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="5f5cc-130">새로운 AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5f5cc-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5f5cc-131">제거-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5f5cc-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5f5cc-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5f5cc-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5f5cc-133">테스트-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5f5cc-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)



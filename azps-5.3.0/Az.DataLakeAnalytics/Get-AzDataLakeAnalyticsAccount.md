---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493488"
---
# <span data-ttu-id="375ea-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="375ea-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="375ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="375ea-102">SYNOPSIS</span></span>
<span data-ttu-id="375ea-103">Data Lake Analytics 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="375ea-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="375ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="375ea-104">SYNTAX</span></span>

### <span data-ttu-id="375ea-105">GetAllInSubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="375ea-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="375ea-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="375ea-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="375ea-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="375ea-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375ea-108">설명</span><span class="sxs-lookup"><span data-stu-id="375ea-108">DESCRIPTION</span></span>
<span data-ttu-id="375ea-109">**Get-AzDataLakeAnalyticsAccount** cmdlet은 Azure Data Lake Analytics 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="375ea-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="375ea-110">예제</span><span class="sxs-lookup"><span data-stu-id="375ea-110">EXAMPLES</span></span>

### <span data-ttu-id="375ea-111">예제 1: Data Lake Analytics 계정에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="375ea-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="375ea-112">이 명령은 ContosoAdlAccount라는 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="375ea-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="375ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="375ea-113">PARAMETERS</span></span>

### <span data-ttu-id="375ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375ea-114">-DefaultProfile</span></span>
<span data-ttu-id="375ea-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="375ea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="375ea-116">-Name</span><span class="sxs-lookup"><span data-stu-id="375ea-116">-Name</span></span>
<span data-ttu-id="375ea-117">Data Lake Analytics 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="375ea-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="375ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="375ea-119">Data Lake Analytics 계정의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="375ea-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="375ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375ea-120">CommonParameters</span></span>
<span data-ttu-id="375ea-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="375ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375ea-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="375ea-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375ea-123">입력</span><span class="sxs-lookup"><span data-stu-id="375ea-123">INPUTS</span></span>

### <span data-ttu-id="375ea-124">System.String</span><span class="sxs-lookup"><span data-stu-id="375ea-124">System.String</span></span>

## <span data-ttu-id="375ea-125">출력</span><span class="sxs-lookup"><span data-stu-id="375ea-125">OUTPUTS</span></span>

### <span data-ttu-id="375ea-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="375ea-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="375ea-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="375ea-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="375ea-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="375ea-128">NOTES</span></span>

## <span data-ttu-id="375ea-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="375ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="375ea-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="375ea-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="375ea-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="375ea-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="375ea-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="375ea-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="375ea-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="375ea-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)



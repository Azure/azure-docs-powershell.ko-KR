---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: dcd44f9b43184ffc36d58bd5b65a065d7e81b4b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964779"
---
# <span data-ttu-id="e0f00-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e0f00-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e0f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f00-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f00-103">Data Lake Analytics 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f00-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e0f00-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0f00-104">SYNTAX</span></span>

### <span data-ttu-id="e0f00-105">GetAllInSubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="e0f00-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f00-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0f00-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0f00-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="e0f00-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0f00-108">설명</span><span class="sxs-lookup"><span data-stu-id="e0f00-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f00-109">**Get-AzDataLakeAnalyticsAccount** cmdlet은 Azure Data Lake Analytics 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f00-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e0f00-110">예제</span><span class="sxs-lookup"><span data-stu-id="e0f00-110">EXAMPLES</span></span>

### <span data-ttu-id="e0f00-111">예제 1: Data Lake Analytics 계정에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="e0f00-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="e0f00-112">이 명령은 ContosoAdlAccount라는 계정에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f00-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="e0f00-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e0f00-113">PARAMETERS</span></span>

### <span data-ttu-id="e0f00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f00-114">-DefaultProfile</span></span>
<span data-ttu-id="e0f00-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e0f00-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0f00-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e0f00-116">-Name</span></span>
<span data-ttu-id="e0f00-117">Data Lake Analytics 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f00-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="e0f00-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f00-118">-ResourceGroupName</span></span>
<span data-ttu-id="e0f00-119">Data Lake Analytics 계정의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f00-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="e0f00-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f00-120">CommonParameters</span></span>
<span data-ttu-id="e0f00-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f00-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f00-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e0f00-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f00-123">입력</span><span class="sxs-lookup"><span data-stu-id="e0f00-123">INPUTS</span></span>

### <span data-ttu-id="e0f00-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e0f00-124">System.String</span></span>

## <span data-ttu-id="e0f00-125">출력</span><span class="sxs-lookup"><span data-stu-id="e0f00-125">OUTPUTS</span></span>

### <span data-ttu-id="e0f00-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e0f00-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="e0f00-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="e0f00-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="e0f00-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e0f00-128">NOTES</span></span>

## <span data-ttu-id="e0f00-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0f00-129">RELATED LINKS</span></span>

[<span data-ttu-id="e0f00-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e0f00-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e0f00-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e0f00-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e0f00-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e0f00-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e0f00-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e0f00-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)



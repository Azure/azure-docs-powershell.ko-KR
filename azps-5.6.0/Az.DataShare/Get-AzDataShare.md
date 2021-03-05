---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: 1cccba1d3af4bcd1ff69ad04f248615e1edb66fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998041"
---
# <span data-ttu-id="0cc77-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="0cc77-101">Get-AzDataShare</span></span>

## <span data-ttu-id="0cc77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cc77-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc77-103">데이터 공유에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0cc77-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="0cc77-104">구문</span><span class="sxs-lookup"><span data-stu-id="0cc77-104">SYNTAX</span></span>

### <span data-ttu-id="0cc77-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0cc77-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cc77-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cc77-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cc77-107">설명</span><span class="sxs-lookup"><span data-stu-id="0cc77-107">DESCRIPTION</span></span>
<span data-ttu-id="0cc77-108">**Get-AzDataShare** cmdlet은 Azure 데이터 공유 accoount의 데이터 공유에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0cc77-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="0cc77-109">데이터 공유의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 공유에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0cc77-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="0cc77-110">이름을 지정하지 않으면 이 cmdlet은 Azure 데이터 공유 계정의 모든 데이터 공유에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc77-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="0cc77-111">예제</span><span class="sxs-lookup"><span data-stu-id="0cc77-111">EXAMPLES</span></span>

### <span data-ttu-id="0cc77-112">예제 1 : 특정 데이터 공유를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cc77-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="0cc77-113">이 명령은 Azure 데이터 공유 계정 WikiAdsAccount 및 리소스 그룹 ADS에서 데이터 공유 AdsShare에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc77-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="0cc77-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0cc77-114">PARAMETERS</span></span>

### <span data-ttu-id="0cc77-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0cc77-115">-AccountName</span></span>
<span data-ttu-id="0cc77-116">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="0cc77-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc77-117">-DefaultProfile</span></span>
<span data-ttu-id="0cc77-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0cc77-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cc77-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0cc77-119">-Name</span></span>
<span data-ttu-id="0cc77-120">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="0cc77-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc77-121">-ResourceGroupName</span></span>
<span data-ttu-id="0cc77-122">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0cc77-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc77-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cc77-123">-ResourceId</span></span>
<span data-ttu-id="0cc77-124">Azure 데이터 공유의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0cc77-124">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cc77-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc77-125">CommonParameters</span></span>
<span data-ttu-id="0cc77-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0cc77-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc77-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cc77-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc77-128">입력</span><span class="sxs-lookup"><span data-stu-id="0cc77-128">INPUTS</span></span>

### <span data-ttu-id="0cc77-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0cc77-129">System.String</span></span>

## <span data-ttu-id="0cc77-130">출력</span><span class="sxs-lookup"><span data-stu-id="0cc77-130">OUTPUTS</span></span>

### <span data-ttu-id="0cc77-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="0cc77-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="0cc77-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0cc77-132">NOTES</span></span>

## <span data-ttu-id="0cc77-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cc77-133">RELATED LINKS</span></span>

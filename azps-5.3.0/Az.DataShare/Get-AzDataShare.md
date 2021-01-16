---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a4c63e22427e3ae0b666bb7d99b8217a990657c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377511"
---
# <span data-ttu-id="34a4b-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="34a4b-101">Get-AzDataShare</span></span>

## <span data-ttu-id="34a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="34a4b-103">데이터 공유에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34a4b-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="34a4b-104">구문</span><span class="sxs-lookup"><span data-stu-id="34a4b-104">SYNTAX</span></span>

### <span data-ttu-id="34a4b-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="34a4b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34a4b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34a4b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34a4b-107">설명</span><span class="sxs-lookup"><span data-stu-id="34a4b-107">DESCRIPTION</span></span>
<span data-ttu-id="34a4b-108">**Get-AzDataShare** cmdlet은 Azure 데이터 공유 계정을 사용하여 데이터 공유에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34a4b-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="34a4b-109">데이터 공유의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 공유에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34a4b-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="34a4b-110">이름을 지정하지 않으면 이 cmdlet은 Azure 데이터 공유 계정의 모든 데이터 공유에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34a4b-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="34a4b-111">예제</span><span class="sxs-lookup"><span data-stu-id="34a4b-111">EXAMPLES</span></span>

### <span data-ttu-id="34a4b-112">예제 1: 특정 데이터 공유를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34a4b-112">Example 1 : Get a specific data share</span></span>
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

<span data-ttu-id="34a4b-113">이 명령은 Azure 데이터 공유 계정 WikiAdsAccount 및 리소스 그룹 ADS의 데이터 공유 AdsShare에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="34a4b-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="34a4b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34a4b-114">PARAMETERS</span></span>

### <span data-ttu-id="34a4b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34a4b-115">-AccountName</span></span>
<span data-ttu-id="34a4b-116">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="34a4b-116">Azure data share account name</span></span>

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

### <span data-ttu-id="34a4b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a4b-117">-DefaultProfile</span></span>
<span data-ttu-id="34a4b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34a4b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a4b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="34a4b-119">-Name</span></span>
<span data-ttu-id="34a4b-120">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="34a4b-120">Azure data share name</span></span>

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

### <span data-ttu-id="34a4b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a4b-121">-ResourceGroupName</span></span>
<span data-ttu-id="34a4b-122">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="34a4b-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="34a4b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34a4b-123">-ResourceId</span></span>
<span data-ttu-id="34a4b-124">Azure 데이터 공유의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="34a4b-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="34a4b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a4b-125">CommonParameters</span></span>
<span data-ttu-id="34a4b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34a4b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a4b-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34a4b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a4b-128">입력</span><span class="sxs-lookup"><span data-stu-id="34a4b-128">INPUTS</span></span>

### <span data-ttu-id="34a4b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="34a4b-129">System.String</span></span>

## <span data-ttu-id="34a4b-130">출력</span><span class="sxs-lookup"><span data-stu-id="34a4b-130">OUTPUTS</span></span>

### <span data-ttu-id="34a4b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="34a4b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="34a4b-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34a4b-132">NOTES</span></span>

## <span data-ttu-id="34a4b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34a4b-133">RELATED LINKS</span></span>

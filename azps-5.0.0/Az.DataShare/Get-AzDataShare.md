---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a4c63e22427e3ae0b666bb7d99b8217a990657c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305306"
---
# <span data-ttu-id="22de7-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="22de7-101">Get-AzDataShare</span></span>

## <span data-ttu-id="22de7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22de7-102">SYNOPSIS</span></span>
<span data-ttu-id="22de7-103">데이터 공유에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22de7-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="22de7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22de7-104">SYNTAX</span></span>

### <span data-ttu-id="22de7-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="22de7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22de7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22de7-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22de7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="22de7-107">DESCRIPTION</span></span>
<span data-ttu-id="22de7-108">**AzDataShare** Cmdlet은 Azure data share accoount의 데이터 공유에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22de7-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="22de7-109">데이터 공유의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 공유에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22de7-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="22de7-110">이름을 지정 하지 않으면이 cmdlet은 Azure 데이터 공유 계정의 모든 데이터 공유에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22de7-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="22de7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="22de7-111">EXAMPLES</span></span>

### <span data-ttu-id="22de7-112">예제 1: 특정 데이터 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="22de7-112">Example 1 : Get a specific data share</span></span>
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

<span data-ttu-id="22de7-113">이 명령은 Azure data share 계정 WikiAdsAccount 및 리소스 그룹 광고의 data 공유 AdsShare에 대 한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22de7-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="22de7-114">변수</span><span class="sxs-lookup"><span data-stu-id="22de7-114">PARAMETERS</span></span>

### <span data-ttu-id="22de7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22de7-115">-AccountName</span></span>
<span data-ttu-id="22de7-116">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="22de7-116">Azure data share account name</span></span>

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

### <span data-ttu-id="22de7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22de7-117">-DefaultProfile</span></span>
<span data-ttu-id="22de7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22de7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22de7-119">-이름</span><span class="sxs-lookup"><span data-stu-id="22de7-119">-Name</span></span>
<span data-ttu-id="22de7-120">Azure 데이터 공유 이름</span><span class="sxs-lookup"><span data-stu-id="22de7-120">Azure data share name</span></span>

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

### <span data-ttu-id="22de7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22de7-121">-ResourceGroupName</span></span>
<span data-ttu-id="22de7-122">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="22de7-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="22de7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22de7-123">-ResourceId</span></span>
<span data-ttu-id="22de7-124">Azure data share의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="22de7-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="22de7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22de7-125">CommonParameters</span></span>
<span data-ttu-id="22de7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22de7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22de7-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="22de7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22de7-128">입력</span><span class="sxs-lookup"><span data-stu-id="22de7-128">INPUTS</span></span>

### <span data-ttu-id="22de7-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22de7-129">System.String</span></span>

## <span data-ttu-id="22de7-130">출력</span><span class="sxs-lookup"><span data-stu-id="22de7-130">OUTPUTS</span></span>

### <span data-ttu-id="22de7-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="22de7-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="22de7-132">상속자</span><span class="sxs-lookup"><span data-stu-id="22de7-132">NOTES</span></span>

## <span data-ttu-id="22de7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22de7-133">RELATED LINKS</span></span>

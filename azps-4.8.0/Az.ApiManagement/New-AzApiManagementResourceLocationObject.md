---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049235"
---
# <span data-ttu-id="1e358-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="1e358-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="1e358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e358-102">SYNOPSIS</span></span>
<span data-ttu-id="1e358-103">새 리소스 위치 계약을 만듭니다 (게이트웨이에서 사용 됨).</span><span class="sxs-lookup"><span data-stu-id="1e358-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="1e358-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e358-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e358-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e358-105">DESCRIPTION</span></span>
<span data-ttu-id="1e358-106">**새로운 AzApiManagementResourceLocationObject** Cmdlet은 게이트웨이에서 사용 되는 새 리소스 위치 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="1e358-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e358-107">EXAMPLES</span></span>

### <span data-ttu-id="1e358-108">예제 1: 리소스 위치 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="1e358-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="1e358-109">이 명령은 리소스 위치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-109">This command creates a resource location.</span></span>

## <span data-ttu-id="1e358-110">변수</span><span class="sxs-lookup"><span data-stu-id="1e358-110">PARAMETERS</span></span>

### <span data-ttu-id="1e358-111">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="1e358-111">-City</span></span>
<span data-ttu-id="1e358-112">위치 구/군/시.</span><span class="sxs-lookup"><span data-stu-id="1e358-112">Location City.</span></span>
<span data-ttu-id="1e358-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e358-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="1e358-114">-CountryOrRegion</span></span>
<span data-ttu-id="1e358-115">국가 또는 지역 위치</span><span class="sxs-lookup"><span data-stu-id="1e358-115">Location Country or Region.</span></span>
<span data-ttu-id="1e358-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e358-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e358-117">-DefaultProfile</span></span>
<span data-ttu-id="1e358-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e358-119">학구</span><span class="sxs-lookup"><span data-stu-id="1e358-119">-District</span></span>
<span data-ttu-id="1e358-120">위치 학구.</span><span class="sxs-lookup"><span data-stu-id="1e358-120">Location District.</span></span>
<span data-ttu-id="1e358-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e358-122">-이름</span><span class="sxs-lookup"><span data-stu-id="1e358-122">-Name</span></span>
<span data-ttu-id="1e358-123">위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-123">Location Name.</span></span>
<span data-ttu-id="1e358-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e358-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e358-125">CommonParameters</span></span>
<span data-ttu-id="1e358-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e358-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e358-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e358-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e358-128">입력</span><span class="sxs-lookup"><span data-stu-id="1e358-128">INPUTS</span></span>

### <span data-ttu-id="1e358-129">않아야</span><span class="sxs-lookup"><span data-stu-id="1e358-129">None</span></span>

## <span data-ttu-id="1e358-130">출력</span><span class="sxs-lookup"><span data-stu-id="1e358-130">OUTPUTS</span></span>

### <span data-ttu-id="1e358-131">ApiManagement. ServiceManagement. \ PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="1e358-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="1e358-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1e358-132">NOTES</span></span>

## <span data-ttu-id="1e358-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e358-133">RELATED LINKS</span></span>

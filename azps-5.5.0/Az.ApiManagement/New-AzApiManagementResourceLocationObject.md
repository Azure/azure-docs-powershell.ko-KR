---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205656"
---
# <span data-ttu-id="3c05b-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="3c05b-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="3c05b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c05b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c05b-103">새 리소스 위치 계약(게이트웨이에서 사용)을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="3c05b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c05b-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c05b-105">설명</span><span class="sxs-lookup"><span data-stu-id="3c05b-105">DESCRIPTION</span></span>
<span data-ttu-id="3c05b-106">**New-AzApiManagementResourceLocationObject** cmdlet은 새 리소스 위치 계약(게이트웨이에서 사용)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="3c05b-107">예제</span><span class="sxs-lookup"><span data-stu-id="3c05b-107">EXAMPLES</span></span>

### <span data-ttu-id="3c05b-108">예제 1: 리소스 위치 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="3c05b-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="3c05b-109">이 명령은 리소스 위치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-109">This command creates a resource location.</span></span>

## <span data-ttu-id="3c05b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c05b-110">PARAMETERS</span></span>

### <span data-ttu-id="3c05b-111">-City</span><span class="sxs-lookup"><span data-stu-id="3c05b-111">-City</span></span>
<span data-ttu-id="3c05b-112">Location City.</span><span class="sxs-lookup"><span data-stu-id="3c05b-112">Location City.</span></span>
<span data-ttu-id="3c05b-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="3c05b-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="3c05b-114">-CountryOrRegion</span></span>
<span data-ttu-id="3c05b-115">위치 국가 또는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-115">Location Country or Region.</span></span>
<span data-ttu-id="3c05b-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="3c05b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c05b-117">-DefaultProfile</span></span>
<span data-ttu-id="3c05b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c05b-119">-District</span><span class="sxs-lookup"><span data-stu-id="3c05b-119">-District</span></span>
<span data-ttu-id="3c05b-120">Location District.</span><span class="sxs-lookup"><span data-stu-id="3c05b-120">Location District.</span></span>
<span data-ttu-id="3c05b-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="3c05b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3c05b-122">-Name</span></span>
<span data-ttu-id="3c05b-123">위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-123">Location Name.</span></span>
<span data-ttu-id="3c05b-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="3c05b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c05b-125">CommonParameters</span></span>
<span data-ttu-id="3c05b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c05b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c05b-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c05b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c05b-128">입력</span><span class="sxs-lookup"><span data-stu-id="3c05b-128">INPUTS</span></span>

### <span data-ttu-id="3c05b-129">없음</span><span class="sxs-lookup"><span data-stu-id="3c05b-129">None</span></span>

## <span data-ttu-id="3c05b-130">출력</span><span class="sxs-lookup"><span data-stu-id="3c05b-130">OUTPUTS</span></span>

### <span data-ttu-id="3c05b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="3c05b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="3c05b-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c05b-132">NOTES</span></span>

## <span data-ttu-id="3c05b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c05b-133">RELATED LINKS</span></span>

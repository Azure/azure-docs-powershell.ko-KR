---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493980"
---
# <span data-ttu-id="965b8-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="965b8-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="965b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="965b8-102">SYNOPSIS</span></span>
<span data-ttu-id="965b8-103">CDN 프로필의 리소스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="965b8-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="965b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="965b8-104">SYNTAX</span></span>

### <span data-ttu-id="965b8-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="965b8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="965b8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="965b8-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="965b8-107">설명</span><span class="sxs-lookup"><span data-stu-id="965b8-107">DESCRIPTION</span></span>
<span data-ttu-id="965b8-108">{{설명 입력}}</span><span class="sxs-lookup"><span data-stu-id="965b8-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="965b8-109">예제</span><span class="sxs-lookup"><span data-stu-id="965b8-109">EXAMPLES</span></span>

### <span data-ttu-id="965b8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="965b8-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="965b8-111">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="965b8-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="965b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="965b8-112">PARAMETERS</span></span>

### <span data-ttu-id="965b8-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="965b8-113">-CdnProfile</span></span>
<span data-ttu-id="965b8-114">Azure CDN 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="965b8-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="965b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965b8-115">-DefaultProfile</span></span>
<span data-ttu-id="965b8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="965b8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="965b8-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="965b8-117">-ProfileName</span></span>
<span data-ttu-id="965b8-118">프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="965b8-118">The name of the profile.</span></span>

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

### <span data-ttu-id="965b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="965b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="965b8-120">프로필이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="965b8-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="965b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965b8-121">CommonParameters</span></span>
<span data-ttu-id="965b8-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="965b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965b8-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="965b8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965b8-124">입력</span><span class="sxs-lookup"><span data-stu-id="965b8-124">INPUTS</span></span>

### <span data-ttu-id="965b8-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="965b8-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="965b8-126">출력</span><span class="sxs-lookup"><span data-stu-id="965b8-126">OUTPUTS</span></span>

### <span data-ttu-id="965b8-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="965b8-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="965b8-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="965b8-128">NOTES</span></span>

## <span data-ttu-id="965b8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="965b8-129">RELATED LINKS</span></span>

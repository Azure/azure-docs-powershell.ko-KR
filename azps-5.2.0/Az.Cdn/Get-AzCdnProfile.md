---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348165"
---
# <span data-ttu-id="22798-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="22798-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="22798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22798-102">SYNOPSIS</span></span>
<span data-ttu-id="22798-103">CDN 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="22798-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="22798-104">구문</span><span class="sxs-lookup"><span data-stu-id="22798-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22798-105">설명</span><span class="sxs-lookup"><span data-stu-id="22798-105">DESCRIPTION</span></span>
<span data-ttu-id="22798-106">**Get-AzCdnProfile** cmdlet은 Azure CDN(Content Delivery Network) 프로필 및 관련 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="22798-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="22798-107">예제</span><span class="sxs-lookup"><span data-stu-id="22798-107">EXAMPLES</span></span>

## <span data-ttu-id="22798-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22798-108">PARAMETERS</span></span>

### <span data-ttu-id="22798-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22798-109">-DefaultProfile</span></span>
<span data-ttu-id="22798-110">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="22798-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22798-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="22798-111">-ProfileName</span></span>
<span data-ttu-id="22798-112">프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22798-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22798-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22798-113">-ResourceGroupName</span></span>
<span data-ttu-id="22798-114">프로필이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22798-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22798-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22798-115">CommonParameters</span></span>
<span data-ttu-id="22798-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22798-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22798-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22798-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22798-118">입력</span><span class="sxs-lookup"><span data-stu-id="22798-118">INPUTS</span></span>

### <span data-ttu-id="22798-119">System.String</span><span class="sxs-lookup"><span data-stu-id="22798-119">System.String</span></span>

## <span data-ttu-id="22798-120">출력</span><span class="sxs-lookup"><span data-stu-id="22798-120">OUTPUTS</span></span>

### <span data-ttu-id="22798-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="22798-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="22798-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22798-122">NOTES</span></span>

## <span data-ttu-id="22798-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22798-123">RELATED LINKS</span></span>

[<span data-ttu-id="22798-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="22798-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="22798-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="22798-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="22798-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="22798-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)



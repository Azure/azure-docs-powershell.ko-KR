---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 82ff7d915a7ddc2d15655513dade28fc1e7ffff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214816"
---
# <span data-ttu-id="8ca69-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="8ca69-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="8ca69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ca69-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca69-103">가상 기기 사이트와 함께 사용할 새 Office 365 트래픽 브레이크 아웃 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca69-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="8ca69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ca69-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ca69-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ca69-105">DESCRIPTION</span></span>
<span data-ttu-id="8ca69-106">New-AzOffice365PolicyProperties 명령은 가상 기기 사이트 woith 사용 되는 Office 365 아웃 브레이크 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca69-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used woith a Virtual Appliance site.</span></span> 

## <span data-ttu-id="8ca69-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ca69-107">EXAMPLES</span></span>

### <span data-ttu-id="8ca69-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ca69-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="8ca69-109">가상 기기 사이트 명령에 사용할 Office 365 트래픽 브레이크 아웃 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ca69-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="8ca69-110">변수</span><span class="sxs-lookup"><span data-stu-id="8ca69-110">PARAMETERS</span></span>

### <span data-ttu-id="8ca69-111">-허용</span><span class="sxs-lookup"><span data-stu-id="8ca69-111">-Allow</span></span>
<span data-ttu-id="8ca69-112">범주 트래픽 허용을 브레이크 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca69-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca69-113">-기본</span><span class="sxs-lookup"><span data-stu-id="8ca69-113">-Default</span></span>
<span data-ttu-id="8ca69-114">기본 범주 소통량을 브레이크 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca69-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca69-115">-DefaultProfile</span></span>
<span data-ttu-id="8ca69-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca69-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ca69-117">-최적화</span><span class="sxs-lookup"><span data-stu-id="8ca69-117">-Optimize</span></span>
<span data-ttu-id="8ca69-118">범주 소통량 최적화를 브레이크 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca69-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca69-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca69-119">CommonParameters</span></span>
<span data-ttu-id="8ca69-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca69-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca69-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8ca69-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca69-122">입력</span><span class="sxs-lookup"><span data-stu-id="8ca69-122">INPUTS</span></span>

### <span data-ttu-id="8ca69-123">않아야</span><span class="sxs-lookup"><span data-stu-id="8ca69-123">None</span></span>

## <span data-ttu-id="8ca69-124">출력</span><span class="sxs-lookup"><span data-stu-id="8ca69-124">OUTPUTS</span></span>

### <span data-ttu-id="8ca69-125">PSOffice365PolicyProperties에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8ca69-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="8ca69-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8ca69-126">NOTES</span></span>

## <span data-ttu-id="8ca69-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ca69-127">RELATED LINKS</span></span>

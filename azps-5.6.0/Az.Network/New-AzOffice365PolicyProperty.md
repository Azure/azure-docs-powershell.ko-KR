---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9e48bfd243133052f526f2b9adcbef2072cdd2cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958352"
---
# <span data-ttu-id="56cdc-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="56cdc-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="56cdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="56cdc-103">Virtual Appliance 사이트와 함께 사용할 새 Office 365 트래픽 중단 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="56cdc-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="56cdc-104">구문</span><span class="sxs-lookup"><span data-stu-id="56cdc-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56cdc-105">설명</span><span class="sxs-lookup"><span data-stu-id="56cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="56cdc-106">New-AzOffice365PolicyProperties 명령은 Virtual Appliance 사이트와 함께 사용할 Office 365 브레이크아웃 정책을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="56cdc-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="56cdc-107">예제</span><span class="sxs-lookup"><span data-stu-id="56cdc-107">EXAMPLES</span></span>

### <span data-ttu-id="56cdc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="56cdc-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="56cdc-109">Virtual Appliance 사이트 명령에 사용할 Office 365 트래픽 중단 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56cdc-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="56cdc-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56cdc-110">PARAMETERS</span></span>

### <span data-ttu-id="56cdc-111">-허용</span><span class="sxs-lookup"><span data-stu-id="56cdc-111">-Allow</span></span>
<span data-ttu-id="56cdc-112">허용 범주 트래픽을 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="56cdc-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="56cdc-113">-Default</span><span class="sxs-lookup"><span data-stu-id="56cdc-113">-Default</span></span>
<span data-ttu-id="56cdc-114">기본 범주 트래픽을 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="56cdc-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="56cdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56cdc-115">-DefaultProfile</span></span>
<span data-ttu-id="56cdc-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56cdc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56cdc-117">-최적화</span><span class="sxs-lookup"><span data-stu-id="56cdc-117">-Optimize</span></span>
<span data-ttu-id="56cdc-118">최적화 범주 트래픽을 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="56cdc-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="56cdc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cdc-119">CommonParameters</span></span>
<span data-ttu-id="56cdc-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56cdc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cdc-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56cdc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cdc-122">입력</span><span class="sxs-lookup"><span data-stu-id="56cdc-122">INPUTS</span></span>

### <span data-ttu-id="56cdc-123">없음</span><span class="sxs-lookup"><span data-stu-id="56cdc-123">None</span></span>

## <span data-ttu-id="56cdc-124">출력</span><span class="sxs-lookup"><span data-stu-id="56cdc-124">OUTPUTS</span></span>

### <span data-ttu-id="56cdc-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="56cdc-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="56cdc-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56cdc-126">NOTES</span></span>

## <span data-ttu-id="56cdc-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56cdc-127">RELATED LINKS</span></span>

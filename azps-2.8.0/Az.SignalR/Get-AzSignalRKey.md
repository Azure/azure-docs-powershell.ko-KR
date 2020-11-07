---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: f0a841ca4cbf0678f831fca590283a6db8ab16b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871482"
---
# <span data-ttu-id="a505c-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="a505c-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="a505c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a505c-102">SYNOPSIS</span></span>
<span data-ttu-id="a505c-103">SignalR 서비스의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a505c-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="a505c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a505c-104">SYNTAX</span></span>

### <span data-ttu-id="a505c-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a505c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a505c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a505c-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a505c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a505c-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a505c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a505c-108">DESCRIPTION</span></span>
<span data-ttu-id="a505c-109">SignalR 서비스의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a505c-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="a505c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a505c-110">EXAMPLES</span></span>

### <span data-ttu-id="a505c-111">특정 SignalR 서비스의 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="a505c-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="a505c-112">파이프의 SignalR service 개체에서 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="a505c-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="a505c-113">변수</span><span class="sxs-lookup"><span data-stu-id="a505c-113">PARAMETERS</span></span>

### <span data-ttu-id="a505c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a505c-114">-DefaultProfile</span></span>
<span data-ttu-id="a505c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a505c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a505c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a505c-116">-InputObject</span></span>
<span data-ttu-id="a505c-117">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a505c-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a505c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a505c-118">-Name</span></span>
<span data-ttu-id="a505c-119">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a505c-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a505c-120">-ResourceGroupName</span></span>
<span data-ttu-id="a505c-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a505c-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a505c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a505c-122">-ResourceId</span></span>
<span data-ttu-id="a505c-123">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a505c-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a505c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a505c-124">CommonParameters</span></span>
<span data-ttu-id="a505c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a505c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a505c-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a505c-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a505c-127">입력</span><span class="sxs-lookup"><span data-stu-id="a505c-127">INPUTS</span></span>

### <span data-ttu-id="a505c-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a505c-128">System.String</span></span>
### <span data-ttu-id="a505c-129">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="a505c-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="a505c-130">출력</span><span class="sxs-lookup"><span data-stu-id="a505c-130">OUTPUTS</span></span>

### <span data-ttu-id="a505c-131">SignalR. PSSignalRKeys/.</span><span class="sxs-lookup"><span data-stu-id="a505c-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="a505c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a505c-132">NOTES</span></span>

## <span data-ttu-id="a505c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a505c-133">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702714"
---
# <span data-ttu-id="726d7-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="726d7-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="726d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="726d7-102">SYNOPSIS</span></span>
<span data-ttu-id="726d7-103">SignalR 서비스의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="726d7-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="726d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="726d7-104">SYNTAX</span></span>

### <span data-ttu-id="726d7-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="726d7-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="726d7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="726d7-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="726d7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="726d7-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="726d7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="726d7-108">DESCRIPTION</span></span>
<span data-ttu-id="726d7-109">SignalR 서비스의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="726d7-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="726d7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="726d7-110">EXAMPLES</span></span>

### <span data-ttu-id="726d7-111">특정 SignalR 서비스의 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="726d7-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="726d7-112">파이프의 SignalR service 개체에서 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="726d7-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="726d7-113">변수</span><span class="sxs-lookup"><span data-stu-id="726d7-113">PARAMETERS</span></span>

### <span data-ttu-id="726d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726d7-114">-DefaultProfile</span></span>
<span data-ttu-id="726d7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="726d7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726d7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="726d7-116">-InputObject</span></span>
<span data-ttu-id="726d7-117">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="726d7-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="726d7-118">-이름</span><span class="sxs-lookup"><span data-stu-id="726d7-118">-Name</span></span>
<span data-ttu-id="726d7-119">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="726d7-119">SignalR service name.</span></span>

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

### <span data-ttu-id="726d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="726d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="726d7-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="726d7-121">Resource group name.</span></span>

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

### <span data-ttu-id="726d7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="726d7-122">-ResourceId</span></span>
<span data-ttu-id="726d7-123">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="726d7-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="726d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726d7-124">CommonParameters</span></span>
<span data-ttu-id="726d7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726d7-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="726d7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726d7-127">입력</span><span class="sxs-lookup"><span data-stu-id="726d7-127">INPUTS</span></span>

### <span data-ttu-id="726d7-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="726d7-128">System.String</span></span>
<span data-ttu-id="726d7-129">매개 변수: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="726d7-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="726d7-130">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="726d7-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="726d7-131">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="726d7-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="726d7-132">출력</span><span class="sxs-lookup"><span data-stu-id="726d7-132">OUTPUTS</span></span>

### <span data-ttu-id="726d7-133">SignalR. PSSignalRKeys/.</span><span class="sxs-lookup"><span data-stu-id="726d7-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="726d7-134">상속자</span><span class="sxs-lookup"><span data-stu-id="726d7-134">NOTES</span></span>

## <span data-ttu-id="726d7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="726d7-135">RELATED LINKS</span></span>

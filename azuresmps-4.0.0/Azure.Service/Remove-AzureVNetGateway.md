---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045490"
---
# <span data-ttu-id="92144-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="92144-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="92144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92144-102">SYNOPSIS</span></span>
<span data-ttu-id="92144-103">VPN 게이트웨이를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92144-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="92144-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92144-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92144-105">설명은</span><span class="sxs-lookup"><span data-stu-id="92144-105">DESCRIPTION</span></span>
<span data-ttu-id="92144-106">**제거-AzureVNetGateway** cmdlet은 가상 네트워크에 대 한 기존 VPN (가상 사설망) 게이트웨이를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92144-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="92144-107">예제의</span><span class="sxs-lookup"><span data-stu-id="92144-107">EXAMPLES</span></span>

### <span data-ttu-id="92144-108">예제 1: 가상 네트워크 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="92144-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="92144-109">이 명령은 ContosoVN07 이라는 가상 네트워크에서 가상 네트워크 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="92144-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="92144-110">변수</span><span class="sxs-lookup"><span data-stu-id="92144-110">PARAMETERS</span></span>

### <span data-ttu-id="92144-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="92144-111">-Profile</span></span>
<span data-ttu-id="92144-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92144-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="92144-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="92144-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92144-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="92144-114">-VNetName</span></span>
<span data-ttu-id="92144-115">이 cmdlet이 VPN 게이트웨이를 삭제 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92144-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92144-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92144-116">CommonParameters</span></span>
<span data-ttu-id="92144-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92144-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92144-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92144-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92144-119">입력</span><span class="sxs-lookup"><span data-stu-id="92144-119">INPUTS</span></span>

## <span data-ttu-id="92144-120">출력</span><span class="sxs-lookup"><span data-stu-id="92144-120">OUTPUTS</span></span>

## <span data-ttu-id="92144-121">상속자</span><span class="sxs-lookup"><span data-stu-id="92144-121">NOTES</span></span>

## <span data-ttu-id="92144-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92144-122">RELATED LINKS</span></span>

[<span data-ttu-id="92144-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="92144-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="92144-124">새-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="92144-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="92144-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="92144-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="92144-126">크기 조정-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="92144-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="92144-127">Set-Azurevnet2| Key</span><span class="sxs-lookup"><span data-stu-id="92144-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)



---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045465"
---
# <span data-ttu-id="ecace-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ecace-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="ecace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecace-102">SYNOPSIS</span></span>
<span data-ttu-id="ecace-103">가상 네트워크 VPN 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecace-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="ecace-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecace-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ecace-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ecace-105">DESCRIPTION</span></span>
<span data-ttu-id="ecace-106">**Reset-AzureVNetGateway** cmdlet은 가상 개인 네트워크 (VPN) 가상 네트워크 게이트웨이를 다시 설정 하 고 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecace-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="ecace-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ecace-107">EXAMPLES</span></span>

### <span data-ttu-id="ecace-108">예제 1: 가상 네트워크 게이트웨이 다시 설정</span><span class="sxs-lookup"><span data-stu-id="ecace-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="ecace-109">이 명령은 ContosoVN07 이라는 가상 네트워크에서 가상 네트워크 게이트웨이를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecace-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="ecace-110">변수</span><span class="sxs-lookup"><span data-stu-id="ecace-110">PARAMETERS</span></span>

### <span data-ttu-id="ecace-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="ecace-111">-Profile</span></span>
<span data-ttu-id="ecace-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecace-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ecace-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ecace-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ecace-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ecace-114">-VNetName</span></span>
<span data-ttu-id="ecace-115">이 cmdlet이 다시 설정 하는 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecace-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="ecace-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecace-116">CommonParameters</span></span>
<span data-ttu-id="ecace-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecace-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecace-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecace-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecace-119">입력</span><span class="sxs-lookup"><span data-stu-id="ecace-119">INPUTS</span></span>

## <span data-ttu-id="ecace-120">출력</span><span class="sxs-lookup"><span data-stu-id="ecace-120">OUTPUTS</span></span>

## <span data-ttu-id="ecace-121">상속자</span><span class="sxs-lookup"><span data-stu-id="ecace-121">NOTES</span></span>

## <span data-ttu-id="ecace-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecace-122">RELATED LINKS</span></span>

[<span data-ttu-id="ecace-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ecace-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="ecace-124">새-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ecace-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="ecace-125">-AzureVNetGateway 제거</span><span class="sxs-lookup"><span data-stu-id="ecace-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="ecace-126">크기 조정-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ecace-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="ecace-127">Set-Azurevnet2| Key</span><span class="sxs-lookup"><span data-stu-id="ecace-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)



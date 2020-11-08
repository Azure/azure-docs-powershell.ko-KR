---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046279"
---
# <span data-ttu-id="488ea-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="488ea-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="488ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="488ea-102">SYNOPSIS</span></span>
<span data-ttu-id="488ea-103">가상 네트워크 게이트웨이의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="488ea-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="488ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="488ea-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="488ea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="488ea-105">DESCRIPTION</span></span>
<span data-ttu-id="488ea-106">**Get-AzureVNetGateway** cmdlet은 기존 가상 네트워크 게이트웨이의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="488ea-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="488ea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="488ea-107">EXAMPLES</span></span>

### <span data-ttu-id="488ea-108">예제 1: 가상 네트워크 게이트웨이의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="488ea-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="488ea-109">이 명령은 ContosoVN07 이라는 가상 네트워크에 대 한 가상 네트워크 게이트웨이의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="488ea-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="488ea-110">변수</span><span class="sxs-lookup"><span data-stu-id="488ea-110">PARAMETERS</span></span>

### <span data-ttu-id="488ea-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="488ea-111">-Profile</span></span>
<span data-ttu-id="488ea-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="488ea-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="488ea-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="488ea-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="488ea-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="488ea-114">-VNetName</span></span>
<span data-ttu-id="488ea-115">이 cmdlet이 상태를 가져올 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="488ea-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="488ea-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="488ea-116">CommonParameters</span></span>
<span data-ttu-id="488ea-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="488ea-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="488ea-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="488ea-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="488ea-119">입력</span><span class="sxs-lookup"><span data-stu-id="488ea-119">INPUTS</span></span>

## <span data-ttu-id="488ea-120">출력</span><span class="sxs-lookup"><span data-stu-id="488ea-120">OUTPUTS</span></span>

## <span data-ttu-id="488ea-121">상속자</span><span class="sxs-lookup"><span data-stu-id="488ea-121">NOTES</span></span>

## <span data-ttu-id="488ea-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="488ea-122">RELATED LINKS</span></span>

[<span data-ttu-id="488ea-123">새-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="488ea-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="488ea-124">-AzureVNetGateway 제거</span><span class="sxs-lookup"><span data-stu-id="488ea-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="488ea-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="488ea-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="488ea-126">크기 조정-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="488ea-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="488ea-127">Set-Azurevnet2| Key</span><span class="sxs-lookup"><span data-stu-id="488ea-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)



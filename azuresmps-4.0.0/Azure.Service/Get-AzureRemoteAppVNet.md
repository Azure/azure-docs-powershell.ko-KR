---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046570"
---
# <span data-ttu-id="fe7b2-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="fe7b2-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="fe7b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7b2-103">Azure에서 Azure RemoteApp 가상 네트워크에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="fe7b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe7b2-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe7b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe7b2-105">DESCRIPTION</span></span>
<span data-ttu-id="fe7b2-106">**AzureRemoteAppVNet** Cmdlet은 Microsoft Azure에서 Azure RemoteApp 가상 네트워크에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="fe7b2-107">이 cmdlet은 지정 된 가상 네트워크에 대 한 정보를 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="fe7b2-108">가상 네트워크를 지정 하지 않으면이 cmdlet은 현재 구독의 모든 가상 네트워크에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="fe7b2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fe7b2-109">EXAMPLES</span></span>

### <span data-ttu-id="fe7b2-110">예제 1: 가상 네트워크에 대 한 정보 검색</span><span class="sxs-lookup"><span data-stu-id="fe7b2-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="fe7b2-111">이 명령은 ContosoVNet 이라는 가상 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="fe7b2-112">변수</span><span class="sxs-lookup"><span data-stu-id="fe7b2-112">PARAMETERS</span></span>

### <span data-ttu-id="fe7b2-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="fe7b2-113">-IncludeSharedKey</span></span>
<span data-ttu-id="fe7b2-114">이 cmdlet에 가상 네트워크에 대해 검색 하는 정보의 공유 키 값이 포함 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe7b2-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="fe7b2-115">-Profile</span></span>
<span data-ttu-id="fe7b2-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe7b2-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe7b2-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="fe7b2-118">-VNetName</span></span>
<span data-ttu-id="fe7b2-119">Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="fe7b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7b2-120">CommonParameters</span></span>
<span data-ttu-id="fe7b2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7b2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe7b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7b2-123">입력</span><span class="sxs-lookup"><span data-stu-id="fe7b2-123">INPUTS</span></span>

## <span data-ttu-id="fe7b2-124">출력</span><span class="sxs-lookup"><span data-stu-id="fe7b2-124">OUTPUTS</span></span>

## <span data-ttu-id="fe7b2-125">상속자</span><span class="sxs-lookup"><span data-stu-id="fe7b2-125">NOTES</span></span>

## <span data-ttu-id="fe7b2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe7b2-126">RELATED LINKS</span></span>

[<span data-ttu-id="fe7b2-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="fe7b2-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)



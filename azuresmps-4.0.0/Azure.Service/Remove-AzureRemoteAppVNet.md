---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046146"
---
# <span data-ttu-id="69ef9-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="69ef9-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="69ef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="69ef9-103">Azure RemoteApp 가상 네트워크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ef9-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="69ef9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69ef9-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69ef9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="69ef9-106">**AzureRemoteAppVNet** Cmdlet은 Azure RemoteApp 가상 네트워크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ef9-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="69ef9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="69ef9-108">예제 1: 지정 된 가상 네트워크 삭제</span><span class="sxs-lookup"><span data-stu-id="69ef9-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="69ef9-109">이 명령은 ContosoVNet 이라는 가상 네트워크를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ef9-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="69ef9-110">변수</span><span class="sxs-lookup"><span data-stu-id="69ef9-110">PARAMETERS</span></span>

### <span data-ttu-id="69ef9-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="69ef9-111">-Profile</span></span>
<span data-ttu-id="69ef9-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ef9-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69ef9-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="69ef9-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69ef9-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="69ef9-114">-VNetName</span></span>
<span data-ttu-id="69ef9-115">삭제할 Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ef9-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ef9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ef9-116">CommonParameters</span></span>
<span data-ttu-id="69ef9-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ef9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ef9-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ef9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ef9-119">입력</span><span class="sxs-lookup"><span data-stu-id="69ef9-119">INPUTS</span></span>

## <span data-ttu-id="69ef9-120">출력</span><span class="sxs-lookup"><span data-stu-id="69ef9-120">OUTPUTS</span></span>

## <span data-ttu-id="69ef9-121">상속자</span><span class="sxs-lookup"><span data-stu-id="69ef9-121">NOTES</span></span>

## <span data-ttu-id="69ef9-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69ef9-122">RELATED LINKS</span></span>

[<span data-ttu-id="69ef9-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="69ef9-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="69ef9-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="69ef9-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)



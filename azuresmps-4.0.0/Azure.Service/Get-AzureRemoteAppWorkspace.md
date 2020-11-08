---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045619"
---
# <span data-ttu-id="1dfd6-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="1dfd6-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="1dfd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dfd6-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfd6-103">Azure RemoteApp 작업 영역에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfd6-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="1dfd6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1dfd6-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1dfd6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1dfd6-105">DESCRIPTION</span></span>
<span data-ttu-id="1dfd6-106">**AzureRemoteAppWorkspace** Cmdlet은 Azure RemoteApp 작업 영역에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfd6-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="1dfd6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1dfd6-107">EXAMPLES</span></span>

### <span data-ttu-id="1dfd6-108">예제 1: 작업 영역에 대 한 정보 검색</span><span class="sxs-lookup"><span data-stu-id="1dfd6-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="1dfd6-109">이 명령은 Azure RemoteApp 작업 영역에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfd6-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="1dfd6-110">변수</span><span class="sxs-lookup"><span data-stu-id="1dfd6-110">PARAMETERS</span></span>

### <span data-ttu-id="1dfd6-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="1dfd6-111">-Profile</span></span>
<span data-ttu-id="1dfd6-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfd6-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1dfd6-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1dfd6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1dfd6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfd6-114">CommonParameters</span></span>
<span data-ttu-id="1dfd6-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfd6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfd6-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dfd6-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfd6-117">입력</span><span class="sxs-lookup"><span data-stu-id="1dfd6-117">INPUTS</span></span>

## <span data-ttu-id="1dfd6-118">출력</span><span class="sxs-lookup"><span data-stu-id="1dfd6-118">OUTPUTS</span></span>

## <span data-ttu-id="1dfd6-119">상속자</span><span class="sxs-lookup"><span data-stu-id="1dfd6-119">NOTES</span></span>

## <span data-ttu-id="1dfd6-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dfd6-120">RELATED LINKS</span></span>

[<span data-ttu-id="1dfd6-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="1dfd6-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)



---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046051"
---
# <span data-ttu-id="eb385-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="eb385-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="eb385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb385-102">SYNOPSIS</span></span>
<span data-ttu-id="eb385-103">Azure RemoteApp 작업 영역의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb385-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="eb385-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb385-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eb385-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eb385-105">DESCRIPTION</span></span>
<span data-ttu-id="eb385-106">**Set-AzureRemoteAppWorkspace** Cmdlet은 Azure RemoteApp 작업 영역의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb385-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="eb385-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eb385-107">EXAMPLES</span></span>

### <span data-ttu-id="eb385-108">예제 1: 작업 영역 이름 설정</span><span class="sxs-lookup"><span data-stu-id="eb385-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="eb385-109">이 명령은 Azure RemoteApp 작업 영역 이름을 Contoso 작업 응용 프로그램으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb385-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="eb385-110">변수</span><span class="sxs-lookup"><span data-stu-id="eb385-110">PARAMETERS</span></span>

### <span data-ttu-id="eb385-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="eb385-111">-Profile</span></span>
<span data-ttu-id="eb385-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb385-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb385-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="eb385-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb385-114">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eb385-114">-WorkspaceName</span></span>
<span data-ttu-id="eb385-115">Azure RemoteApp 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb385-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb385-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb385-116">CommonParameters</span></span>
<span data-ttu-id="eb385-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb385-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb385-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb385-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb385-119">입력</span><span class="sxs-lookup"><span data-stu-id="eb385-119">INPUTS</span></span>

## <span data-ttu-id="eb385-120">출력</span><span class="sxs-lookup"><span data-stu-id="eb385-120">OUTPUTS</span></span>

## <span data-ttu-id="eb385-121">상속자</span><span class="sxs-lookup"><span data-stu-id="eb385-121">NOTES</span></span>
* <span data-ttu-id="eb385-122">지정 된 구독에 대 한 모든 Azure RemoteApp 컬렉션이 공유 작업 영역 내에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb385-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="eb385-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb385-123">RELATED LINKS</span></span>

[<span data-ttu-id="eb385-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="eb385-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)



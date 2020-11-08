---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046322"
---
# <span data-ttu-id="48e3d-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="48e3d-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="48e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="48e3d-103">Azure RemoteApp 작업의 결과를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="48e3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48e3d-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="48e3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48e3d-105">DESCRIPTION</span></span>
<span data-ttu-id="48e3d-106">**AzureRemoteAppOperationResult** cmdlet은 장기 실행 Azure RemoteApp 작업의 결과를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="48e3d-107">Azure RemoteApp은 서비스에서 처리 해야 하며 즉시 반환할 수 없는 많은 작업에 장기 실행 작업을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="48e3d-108">추적 Id를 반환 하는 cmdlet의 예로는 **업데이트-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** 등이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="48e3d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="48e3d-109">EXAMPLES</span></span>

### <span data-ttu-id="48e3d-110">예제 1: 추적 ID를 사용 하 여 작업 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="48e3d-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="48e3d-111">이 명령은 Azure RemoteApp 작업에서 반환 된 추적 ID를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="48e3d-112">추적 ID는 다음 명령에서 **Get-AzureRemoteAppOperationResult** 에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="48e3d-113">변수</span><span class="sxs-lookup"><span data-stu-id="48e3d-113">PARAMETERS</span></span>

### <span data-ttu-id="48e3d-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="48e3d-114">-Profile</span></span>
<span data-ttu-id="48e3d-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48e3d-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48e3d-117">-TrackingId</span><span class="sxs-lookup"><span data-stu-id="48e3d-117">-TrackingId</span></span>
<span data-ttu-id="48e3d-118">작업의 추적 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-118">Specifies the tracking ID of an operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e3d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e3d-119">CommonParameters</span></span>
<span data-ttu-id="48e3d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48e3d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e3d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e3d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e3d-122">입력</span><span class="sxs-lookup"><span data-stu-id="48e3d-122">INPUTS</span></span>

## <span data-ttu-id="48e3d-123">출력</span><span class="sxs-lookup"><span data-stu-id="48e3d-123">OUTPUTS</span></span>

## <span data-ttu-id="48e3d-124">상속자</span><span class="sxs-lookup"><span data-stu-id="48e3d-124">NOTES</span></span>

## <span data-ttu-id="48e3d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48e3d-125">RELATED LINKS</span></span>

[<span data-ttu-id="48e3d-126">연결 해제-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="48e3d-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="48e3d-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="48e3d-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="48e3d-128">업데이트-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="48e3d-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)



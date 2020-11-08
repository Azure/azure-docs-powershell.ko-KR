---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045737"
---
# <span data-ttu-id="b1cb6-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b1cb6-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="b1cb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cb6-103">새 템플릿 이미지를 사용 하 여 Azure RemoteApp 컬렉션을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="b1cb6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1cb6-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1cb6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="b1cb6-106">**업데이트 AzureRemoteAppCollection** cmdlet은 새 템플릿 이미지를 사용 하 여 Azure RemoteApp 컬렉션을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="b1cb6-107">업데이트가 완료 되 면 기존 세션을 사용 하는 사용자는 로그 아웃 하는 데 1 시간 후에 자동으로 로그 아웃 됩니다. 다시 로그인 하면 새로 업데이트 된 컬렉션에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="b1cb6-108">컬렉션이 업데이트 되는 즉시 사용자에 게 즉시 로그 아웃 하려면 *ForceLogoffWhenUpdateComplete* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="b1cb6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b1cb6-109">EXAMPLES</span></span>

## <span data-ttu-id="b1cb6-110">변수</span><span class="sxs-lookup"><span data-stu-id="b1cb6-110">PARAMETERS</span></span>

### <span data-ttu-id="b1cb6-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="b1cb6-111">-CollectionName</span></span>
<span data-ttu-id="b1cb6-112">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1cb6-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="b1cb6-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="b1cb6-114">이 cmdlet이 업데이트가 완료 되는 즉시 기존 세션에서 사용자에 게 로그인 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="b1cb6-115">사용자가 다시 로그인 하면 새로 업데이트 된 컬렉션에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-115">When users sign in again, they connect to the newly updated collection.</span></span>

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

### <span data-ttu-id="b1cb6-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b1cb6-116">-ImageName</span></span>
<span data-ttu-id="b1cb6-117">Azure RemoteApp 템플릿 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-117">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1cb6-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="b1cb6-118">-Profile</span></span>
<span data-ttu-id="b1cb6-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1cb6-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1cb6-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b1cb6-121">-SubnetName</span></span>
<span data-ttu-id="b1cb6-122">컬렉션을 이동할 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-122">Specifies the name of the subnet into which to move the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1cb6-123">-확인</span><span class="sxs-lookup"><span data-stu-id="b1cb6-123">-Confirm</span></span>
<span data-ttu-id="b1cb6-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cb6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1cb6-125">-WhatIf</span></span>
<span data-ttu-id="b1cb6-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1cb6-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1cb6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cb6-128">CommonParameters</span></span>
<span data-ttu-id="b1cb6-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cb6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cb6-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1cb6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cb6-131">입력</span><span class="sxs-lookup"><span data-stu-id="b1cb6-131">INPUTS</span></span>

## <span data-ttu-id="b1cb6-132">출력</span><span class="sxs-lookup"><span data-stu-id="b1cb6-132">OUTPUTS</span></span>

## <span data-ttu-id="b1cb6-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b1cb6-133">NOTES</span></span>

## <span data-ttu-id="b1cb6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1cb6-134">RELATED LINKS</span></span>

[<span data-ttu-id="b1cb6-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b1cb6-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="b1cb6-136">새로운 AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b1cb6-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="b1cb6-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b1cb6-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)



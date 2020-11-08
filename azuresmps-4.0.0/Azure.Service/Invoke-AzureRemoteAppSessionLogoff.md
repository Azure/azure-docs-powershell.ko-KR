---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046247"
---
# <span data-ttu-id="e78e1-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="e78e1-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="e78e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e78e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e78e1-103">Azure RemoteApp 세션을 즉시 로그 오프 합니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="e78e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e78e1-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e78e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e78e1-105">DESCRIPTION</span></span>
<span data-ttu-id="e78e1-106">**AzureRemoteAppSessionLogoff** Cmdlet은 Azure RemoteApp에서 실행 되는 원격 세션에서 사용자를 즉시 로그 오프 합니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="e78e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e78e1-107">EXAMPLES</span></span>

### <span data-ttu-id="e78e1-108">예제 1: 사용자 로그 오프</span><span class="sxs-lookup"><span data-stu-id="e78e1-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="e78e1-109">이 명령은 UPN이 있는 사용자를 로그 오프 PattiFuller@contoso.com 합니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="e78e1-110">변수</span><span class="sxs-lookup"><span data-stu-id="e78e1-110">PARAMETERS</span></span>

### <span data-ttu-id="e78e1-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e78e1-111">-CollectionName</span></span>
<span data-ttu-id="e78e1-112">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="e78e1-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="e78e1-113">-Profile</span></span>
<span data-ttu-id="e78e1-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e78e1-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e78e1-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="e78e1-116">-UserUpn</span></span>
<span data-ttu-id="e78e1-117">예를 들어 사용자의 UPN (사용자 계정 이름)을 PattiFuller@contoso.com 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e78e1-118">-확인</span><span class="sxs-lookup"><span data-stu-id="e78e1-118">-Confirm</span></span>
<span data-ttu-id="e78e1-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e78e1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e78e1-120">-WhatIf</span></span>
<span data-ttu-id="e78e1-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e78e1-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e78e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e78e1-123">CommonParameters</span></span>
<span data-ttu-id="e78e1-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e78e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e78e1-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e78e1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e78e1-126">입력</span><span class="sxs-lookup"><span data-stu-id="e78e1-126">INPUTS</span></span>

## <span data-ttu-id="e78e1-127">출력</span><span class="sxs-lookup"><span data-stu-id="e78e1-127">OUTPUTS</span></span>

## <span data-ttu-id="e78e1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e78e1-128">NOTES</span></span>

## <span data-ttu-id="e78e1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e78e1-129">RELATED LINKS</span></span>

[<span data-ttu-id="e78e1-130">추가-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="e78e1-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="e78e1-131">연결 해제-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="e78e1-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="e78e1-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="e78e1-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)



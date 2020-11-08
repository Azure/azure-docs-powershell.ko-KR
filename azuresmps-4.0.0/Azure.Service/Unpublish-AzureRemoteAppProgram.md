---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046020"
---
# <span data-ttu-id="efd9f-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="efd9f-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="efd9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd9f-102">SYNOPSIS</span></span>
<span data-ttu-id="efd9f-103">Azure RemoteApp 프로그램을 게시 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="efd9f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efd9f-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd9f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="efd9f-105">DESCRIPTION</span></span>
<span data-ttu-id="efd9f-106">AzureRemoteAppProgram cmdlet은 Azure RemoteApp 프로그램을 게시 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="efd9f-107">프로그램의 게시를 취소 한 후에는 Azure RemoteApp 컬렉션의 사용자가 더 이상 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="efd9f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="efd9f-108">EXAMPLES</span></span>

## <span data-ttu-id="efd9f-109">변수</span><span class="sxs-lookup"><span data-stu-id="efd9f-109">PARAMETERS</span></span>

### <span data-ttu-id="efd9f-110">-별칭</span><span class="sxs-lookup"><span data-stu-id="efd9f-110">-Alias</span></span>
<span data-ttu-id="efd9f-111">게시 취소할 프로그램의 별칭 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="efd9f-112">**AzureRemoteAppProgram** 를 사용 하 여 프로그램의 별칭을 검색 하 여 게시 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efd9f-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="efd9f-113">-CollectionName</span></span>
<span data-ttu-id="efd9f-114">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="efd9f-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="efd9f-115">-Profile</span></span>
<span data-ttu-id="efd9f-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="efd9f-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="efd9f-118">-확인</span><span class="sxs-lookup"><span data-stu-id="efd9f-118">-Confirm</span></span>
<span data-ttu-id="efd9f-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd9f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd9f-120">-WhatIf</span></span>
<span data-ttu-id="efd9f-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efd9f-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd9f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd9f-123">CommonParameters</span></span>
<span data-ttu-id="efd9f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd9f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd9f-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efd9f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd9f-126">입력</span><span class="sxs-lookup"><span data-stu-id="efd9f-126">INPUTS</span></span>

## <span data-ttu-id="efd9f-127">출력</span><span class="sxs-lookup"><span data-stu-id="efd9f-127">OUTPUTS</span></span>

## <span data-ttu-id="efd9f-128">상속자</span><span class="sxs-lookup"><span data-stu-id="efd9f-128">NOTES</span></span>

## <span data-ttu-id="efd9f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efd9f-129">RELATED LINKS</span></span>

[<span data-ttu-id="efd9f-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="efd9f-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="efd9f-131">게시-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="efd9f-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)



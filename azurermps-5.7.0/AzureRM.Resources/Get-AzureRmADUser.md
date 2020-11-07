---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703236"
---
# <span data-ttu-id="17ffa-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="17ffa-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="17ffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="17ffa-103">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17ffa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17ffa-104">SYNTAX</span></span>

### <span data-ttu-id="17ffa-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="17ffa-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17ffa-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="17ffa-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17ffa-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17ffa-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17ffa-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="17ffa-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17ffa-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="17ffa-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17ffa-110">설명은</span><span class="sxs-lookup"><span data-stu-id="17ffa-110">DESCRIPTION</span></span>
<span data-ttu-id="17ffa-111">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-111">Filters active directory users.</span></span>

## <span data-ttu-id="17ffa-112">예제의</span><span class="sxs-lookup"><span data-stu-id="17ffa-112">EXAMPLES</span></span>

### <span data-ttu-id="17ffa-113">UPN을 사용 하 여 사용자 필터링</span><span class="sxs-lookup"><span data-stu-id="17ffa-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="17ffa-114">사용자를 가져옵니다. foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="17ffa-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="17ffa-115">검색 문자열을 사용 하 여 사용자 필터링</span><span class="sxs-lookup"><span data-stu-id="17ffa-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="17ffa-116">표시 이름에 Joe가 있는 모든 광고 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="17ffa-117">광고 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="17ffa-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="17ffa-118">모든 광고 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-118">Gets all AD users</span></span>

## <span data-ttu-id="17ffa-119">변수</span><span class="sxs-lookup"><span data-stu-id="17ffa-119">PARAMETERS</span></span>

### <span data-ttu-id="17ffa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ffa-120">-DefaultProfile</span></span>
<span data-ttu-id="17ffa-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="17ffa-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ffa-122">-메일</span><span class="sxs-lookup"><span data-stu-id="17ffa-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ffa-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="17ffa-123">-ObjectId</span></span>
<span data-ttu-id="17ffa-124">사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-124">Object id of the user.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ffa-125">-SearchString</span><span class="sxs-lookup"><span data-stu-id="17ffa-125">-SearchString</span></span>
<span data-ttu-id="17ffa-126">사용자 표시 이름</span><span class="sxs-lookup"><span data-stu-id="17ffa-126">The user display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ffa-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="17ffa-127">-UserPrincipalName</span></span>
<span data-ttu-id="17ffa-128">사용자의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ffa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ffa-129">CommonParameters</span></span>
<span data-ttu-id="17ffa-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ffa-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17ffa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ffa-132">입력</span><span class="sxs-lookup"><span data-stu-id="17ffa-132">INPUTS</span></span>

### <span data-ttu-id="17ffa-133">않아야</span><span class="sxs-lookup"><span data-stu-id="17ffa-133">None</span></span>
<span data-ttu-id="17ffa-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17ffa-135">출력</span><span class="sxs-lookup"><span data-stu-id="17ffa-135">OUTPUTS</span></span>

### <span data-ttu-id="17ffa-136">ActiveDirectory에서 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 목록 '이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17ffa-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="17ffa-137">상속자</span><span class="sxs-lookup"><span data-stu-id="17ffa-137">NOTES</span></span>

## <span data-ttu-id="17ffa-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17ffa-138">RELATED LINKS</span></span>

[<span data-ttu-id="17ffa-139">새로운 AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="17ffa-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="17ffa-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="17ffa-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="17ffa-141">제거-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="17ffa-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)


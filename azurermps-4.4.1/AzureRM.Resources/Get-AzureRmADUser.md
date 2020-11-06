---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: dd864d11608c33f758e0995d9dacf4afc454130a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527316"
---
# <span data-ttu-id="dab95-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="dab95-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="dab95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dab95-102">SYNOPSIS</span></span>
<span data-ttu-id="dab95-103">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dab95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dab95-104">SYNTAX</span></span>

### <span data-ttu-id="dab95-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dab95-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dab95-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dab95-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dab95-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dab95-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dab95-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dab95-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dab95-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="dab95-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dab95-110">설명은</span><span class="sxs-lookup"><span data-stu-id="dab95-110">DESCRIPTION</span></span>
<span data-ttu-id="dab95-111">Active directory 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-111">Filters active directory users.</span></span>

## <span data-ttu-id="dab95-112">예제의</span><span class="sxs-lookup"><span data-stu-id="dab95-112">EXAMPLES</span></span>

### <span data-ttu-id="dab95-113">--------------------------UPN을 사용 하 여 사용자를 필터링--------------------------</span><span class="sxs-lookup"><span data-stu-id="dab95-113">--------------------------  Filters users using UPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="dab95-114">사용자를 가져옵니다. foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="dab95-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="dab95-115">검색 문자열을 사용 하 여 사용자가--------------------------필터링--------------------------</span><span class="sxs-lookup"><span data-stu-id="dab95-115">--------------------------  Filters users using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="dab95-116">표시 이름에 Joe가 있는 모든 광고 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="dab95-117">광고 사용자 목록----------------------------------------------------</span><span class="sxs-lookup"><span data-stu-id="dab95-117">--------------------------  List AD users  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="dab95-118">모든 광고 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-118">Gets all AD users</span></span>

## <span data-ttu-id="dab95-119">변수</span><span class="sxs-lookup"><span data-stu-id="dab95-119">PARAMETERS</span></span>

### <span data-ttu-id="dab95-120">-메일</span><span class="sxs-lookup"><span data-stu-id="dab95-120">-Mail</span></span>
```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dab95-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dab95-121">-ObjectId</span></span>
<span data-ttu-id="dab95-122">사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-122">Object id of the user.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dab95-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="dab95-123">-SearchString</span></span>
<span data-ttu-id="dab95-124">사용자 표시 이름</span><span class="sxs-lookup"><span data-stu-id="dab95-124">The user display name</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dab95-125">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dab95-125">-UserPrincipalName</span></span>
<span data-ttu-id="dab95-126">사용자의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-126">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dab95-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab95-127">-DefaultProfile</span></span>
<span data-ttu-id="dab95-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab95-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab95-129">CommonParameters</span></span>
<span data-ttu-id="dab95-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab95-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dab95-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab95-132">입력</span><span class="sxs-lookup"><span data-stu-id="dab95-132">INPUTS</span></span>

## <span data-ttu-id="dab95-133">출력</span><span class="sxs-lookup"><span data-stu-id="dab95-133">OUTPUTS</span></span>

### <span data-ttu-id="dab95-134">ActiveDirectory에서 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 목록 '이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dab95-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="dab95-135">상속자</span><span class="sxs-lookup"><span data-stu-id="dab95-135">NOTES</span></span>

## <span data-ttu-id="dab95-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dab95-136">RELATED LINKS</span></span>

[<span data-ttu-id="dab95-137">새로운 AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="dab95-137">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="dab95-138">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="dab95-138">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="dab95-139">제거-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="dab95-139">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)


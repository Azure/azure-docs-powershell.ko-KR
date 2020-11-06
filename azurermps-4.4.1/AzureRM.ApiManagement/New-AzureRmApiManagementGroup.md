---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 8fc237b130e5044e52f47d306d04c42d12fbad81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531266"
---
# <span data-ttu-id="2b843-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2b843-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="2b843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b843-102">SYNOPSIS</span></span>
<span data-ttu-id="2b843-103">API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b843-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b843-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b843-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b843-105">DESCRIPTION</span></span>
<span data-ttu-id="2b843-106">**AzureRmApiManagementGroup** CMDLET은 API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="2b843-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b843-107">EXAMPLES</span></span>

### <span data-ttu-id="2b843-108">예제 1: 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="2b843-108">Example 1: Create a management group</span></span>
```
PS C:\>New-AzureRmApiManagementGroup -Context $APImContext -Name "Group0001"
```

<span data-ttu-id="2b843-109">이 명령은 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-109">This command creates a management group.</span></span>

## <span data-ttu-id="2b843-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b843-110">PARAMETERS</span></span>

### <span data-ttu-id="2b843-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2b843-111">-Context</span></span>
<span data-ttu-id="2b843-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b843-113">-설명</span><span class="sxs-lookup"><span data-stu-id="2b843-113">-Description</span></span>
<span data-ttu-id="2b843-114">관리 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-114">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b843-115">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="2b843-115">-ExternalId</span></span>
<span data-ttu-id="2b843-116">외부 그룹의 경우이 속성에는 외부 id 공급자 (예: Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c)의 그룹 id가 포함 됩니다. 그렇지 않으면 값이 null입니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-116">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b843-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2b843-117">-GroupId</span></span>
<span data-ttu-id="2b843-118">새 관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-118">Specifies the identifier of the new management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b843-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2b843-119">-Name</span></span>
<span data-ttu-id="2b843-120">관리 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-120">Specifies the management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b843-121">-Type</span><span class="sxs-lookup"><span data-stu-id="2b843-121">-Type</span></span>
<span data-ttu-id="2b843-122">그룹 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-122">Group Type.</span></span> <span data-ttu-id="2b843-123">사용자 지정 그룹은 사용자가 정의한 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-123">Custom Group is User defined Group.</span></span> <span data-ttu-id="2b843-124">시스템 그룹에는 관리자, 개발자, 게스트 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-124">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="2b843-125">시스템 그룹을 만들거나 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-125">You cannot create or update a System Group.</span></span>  <span data-ttu-id="2b843-126">외부 그룹은 Azure Active Directory와 같은 외부 Id 공급자의 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-126">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="2b843-127">이 매개 변수는 선택 사항이 며 기본적으로 사용자 지정 그룹으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-127">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b843-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b843-128">-DefaultProfile</span></span>
<span data-ttu-id="2b843-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b843-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b843-130">CommonParameters</span></span>
<span data-ttu-id="2b843-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b843-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b843-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b843-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b843-133">입력</span><span class="sxs-lookup"><span data-stu-id="2b843-133">INPUTS</span></span>

## <span data-ttu-id="2b843-134">출력</span><span class="sxs-lookup"><span data-stu-id="2b843-134">OUTPUTS</span></span>

### <span data-ttu-id="2b843-135">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2b843-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="2b843-136">상속자</span><span class="sxs-lookup"><span data-stu-id="2b843-136">NOTES</span></span>

## <span data-ttu-id="2b843-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b843-137">RELATED LINKS</span></span>

[<span data-ttu-id="2b843-138">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2b843-138">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="2b843-139">제거-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2b843-139">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="2b843-140">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2b843-140">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 22feec8308b682aa2290de6bd8b7361bb07cd560
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701672"
---
# <span data-ttu-id="b675c-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b675c-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="b675c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b675c-102">SYNOPSIS</span></span>
<span data-ttu-id="b675c-103">API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-103">Creates an API management group.</span></span>

## <span data-ttu-id="b675c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b675c-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b675c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b675c-105">DESCRIPTION</span></span>
<span data-ttu-id="b675c-106">**AzApiManagementGroup** CMDLET은 API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="b675c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b675c-107">EXAMPLES</span></span>

### <span data-ttu-id="b675c-108">예제 1: 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="b675c-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="b675c-109">이 명령은 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-109">This command creates a management group.</span></span>

## <span data-ttu-id="b675c-110">변수</span><span class="sxs-lookup"><span data-stu-id="b675c-110">PARAMETERS</span></span>

### <span data-ttu-id="b675c-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b675c-111">-Context</span></span>
<span data-ttu-id="b675c-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b675c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b675c-113">-DefaultProfile</span></span>
<span data-ttu-id="b675c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b675c-115">-설명</span><span class="sxs-lookup"><span data-stu-id="b675c-115">-Description</span></span>
<span data-ttu-id="b675c-116">관리 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="b675c-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="b675c-117">-ExternalId</span></span>
<span data-ttu-id="b675c-118">외부 그룹의 경우이 속성에는 외부 id 공급자 (예: Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c)의 그룹 id가 포함 됩니다. 그렇지 않으면 값이 null입니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="b675c-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b675c-119">-GroupId</span></span>
<span data-ttu-id="b675c-120">새 관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="b675c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b675c-121">-Name</span></span>
<span data-ttu-id="b675c-122">관리 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="b675c-123">-Type</span><span class="sxs-lookup"><span data-stu-id="b675c-123">-Type</span></span>
<span data-ttu-id="b675c-124">그룹 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-124">Group Type.</span></span> <span data-ttu-id="b675c-125">사용자 지정 그룹은 사용자가 정의한 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="b675c-126">시스템 그룹에는 관리자, 개발자, 게스트 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="b675c-127">시스템 그룹을 만들거나 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="b675c-128">외부 그룹은 Azure Active Directory와 같은 외부 Id 공급자의 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="b675c-129">이 매개 변수는 선택 사항이 며 기본적으로 사용자 지정 그룹으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b675c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b675c-130">CommonParameters</span></span>
<span data-ttu-id="b675c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b675c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b675c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b675c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b675c-133">입력</span><span class="sxs-lookup"><span data-stu-id="b675c-133">INPUTS</span></span>

### <span data-ttu-id="b675c-134">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b675c-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b675c-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b675c-135">System.String</span></span>

### <span data-ttu-id="b675c-136">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementGroupType, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b675c-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b675c-137">출력</span><span class="sxs-lookup"><span data-stu-id="b675c-137">OUTPUTS</span></span>

### <span data-ttu-id="b675c-138">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b675c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="b675c-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b675c-139">NOTES</span></span>

## <span data-ttu-id="b675c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b675c-140">RELATED LINKS</span></span>

[<span data-ttu-id="b675c-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b675c-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="b675c-142">제거-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b675c-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="b675c-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b675c-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)



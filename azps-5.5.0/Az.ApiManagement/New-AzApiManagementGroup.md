---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 4400cb375b60b4f961831927ed5763c608f8e5f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195388"
---
# <span data-ttu-id="647c6-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="647c6-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="647c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="647c6-102">SYNOPSIS</span></span>
<span data-ttu-id="647c6-103">API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-103">Creates an API management group.</span></span>

## <span data-ttu-id="647c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="647c6-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="647c6-105">설명</span><span class="sxs-lookup"><span data-stu-id="647c6-105">DESCRIPTION</span></span>
<span data-ttu-id="647c6-106">**New-AzApiManagementGroup** cmdlet은 API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="647c6-107">예제</span><span class="sxs-lookup"><span data-stu-id="647c6-107">EXAMPLES</span></span>

### <span data-ttu-id="647c6-108">예제 1: 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="647c6-108">Example 1: Create a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="647c6-109">이 명령은 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-109">This command creates a management group.</span></span>

### <span data-ttu-id="647c6-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="647c6-110">Example 2</span></span>

<span data-ttu-id="647c6-111">API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-111">Creates an API management group.</span></span> <span data-ttu-id="647c6-112">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="647c6-112">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementGroup -Context <PsApiManagementContext> -Description 'Create Echo Api V4' -GroupId '0001' -Name 'Group0001' -Type Custom
```

## <span data-ttu-id="647c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="647c6-113">PARAMETERS</span></span>

### <span data-ttu-id="647c6-114">-Context</span><span class="sxs-lookup"><span data-stu-id="647c6-114">-Context</span></span>
<span data-ttu-id="647c6-115">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-115">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="647c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647c6-116">-DefaultProfile</span></span>
<span data-ttu-id="647c6-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="647c6-118">-Description</span><span class="sxs-lookup"><span data-stu-id="647c6-118">-Description</span></span>
<span data-ttu-id="647c6-119">관리 그룹의 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-119">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="647c6-120">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="647c6-120">-ExternalId</span></span>
<span data-ttu-id="647c6-121">외부 그룹의 경우 이 속성에는 외부 ID 공급자의 그룹 ID(예: Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c. 그렇지 않으면 값이 null입니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-121">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="647c6-122">-GroupId</span><span class="sxs-lookup"><span data-stu-id="647c6-122">-GroupId</span></span>
<span data-ttu-id="647c6-123">새 관리 그룹의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-123">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="647c6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="647c6-124">-Name</span></span>
<span data-ttu-id="647c6-125">관리 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-125">Specifies the management group name.</span></span>

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

### <span data-ttu-id="647c6-126">-Type</span><span class="sxs-lookup"><span data-stu-id="647c6-126">-Type</span></span>
<span data-ttu-id="647c6-127">그룹 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-127">Group Type.</span></span> <span data-ttu-id="647c6-128">사용자 지정 그룹은 사용자 정의 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-128">Custom Group is User defined Group.</span></span> <span data-ttu-id="647c6-129">시스템 그룹에는 관리자, 개발자 및 게스트가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-129">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="647c6-130">시스템 그룹을 만들거나 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-130">You cannot create or update a System Group.</span></span>  <span data-ttu-id="647c6-131">외부 그룹은 Azure Active Directory와 같은 외부 ID 공급자의 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-131">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="647c6-132">이 매개 변수는 선택 사항이며 기본적으로 사용자 지정 그룹으로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-132">This parameter is optional and by default assumed to be a Custom Group.</span></span>

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

### <span data-ttu-id="647c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647c6-133">CommonParameters</span></span>
<span data-ttu-id="647c6-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="647c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647c6-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="647c6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647c6-136">입력</span><span class="sxs-lookup"><span data-stu-id="647c6-136">INPUTS</span></span>

### <span data-ttu-id="647c6-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="647c6-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="647c6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="647c6-138">System.String</span></span>

### <span data-ttu-id="647c6-139">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="647c6-139">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="647c6-140">출력</span><span class="sxs-lookup"><span data-stu-id="647c6-140">OUTPUTS</span></span>

### <span data-ttu-id="647c6-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="647c6-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="647c6-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="647c6-142">NOTES</span></span>

## <span data-ttu-id="647c6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="647c6-143">RELATED LINKS</span></span>

[<span data-ttu-id="647c6-144">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="647c6-144">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="647c6-145">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="647c6-145">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="647c6-146">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="647c6-146">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


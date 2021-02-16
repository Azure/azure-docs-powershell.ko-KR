---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207429"
---
# <span data-ttu-id="947ed-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="947ed-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="947ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="947ed-102">SYNOPSIS</span></span>
<span data-ttu-id="947ed-103">기본 사이트 Access Restiction 구성의 상속을 Azure 웹앱에 대한 SCM 사이트로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="947ed-104">구문</span><span class="sxs-lookup"><span data-stu-id="947ed-104">SYNTAX</span></span>

### <span data-ttu-id="947ed-105">InputValuesParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="947ed-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947ed-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="947ed-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="947ed-107">설명</span><span class="sxs-lookup"><span data-stu-id="947ed-107">DESCRIPTION</span></span>
<span data-ttu-id="947ed-108">**Update-AzWebAppAccessRestrictionConfig** cmdlet은 Azure 웹앱에 대한 액세스 제한 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="947ed-109">예제</span><span class="sxs-lookup"><span data-stu-id="947ed-109">EXAMPLES</span></span>

### <span data-ttu-id="947ed-110">예제 1: 기본 사이트의 액세스 제한을 사용하여 웹앱 SCM 사이트 업데이트</span><span class="sxs-lookup"><span data-stu-id="947ed-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="947ed-111">다음 예제에서는 리소스 그룹 MyResourceGroup에 속하는 IpRule이라는 웹앱을 업데이트하여 scm 사이트의 기본 사이트의 액세스 제한 구성을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="947ed-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="947ed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="947ed-112">PARAMETERS</span></span>

### <span data-ttu-id="947ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947ed-113">-DefaultProfile</span></span>
<span data-ttu-id="947ed-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="947ed-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="947ed-115">-InputObject</span></span>
<span data-ttu-id="947ed-116">액세스 제한 구성 개체</span><span class="sxs-lookup"><span data-stu-id="947ed-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="947ed-117">-Name</span><span class="sxs-lookup"><span data-stu-id="947ed-117">-Name</span></span>
<span data-ttu-id="947ed-118">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="947ed-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947ed-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="947ed-119">-PassThru</span></span>
<span data-ttu-id="947ed-120">액세스 제한 구성 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-120">Return the access restriction config object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="947ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="947ed-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="947ed-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947ed-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="947ed-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="947ed-124">Scm 사이트는 기본 사이트에 설정된 규칙을 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947ed-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="947ed-125">-SlotName</span></span>
<span data-ttu-id="947ed-126">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947ed-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="947ed-127">-Confirm</span></span>
<span data-ttu-id="947ed-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="947ed-129">-WhatIf</span></span>
<span data-ttu-id="947ed-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="947ed-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="947ed-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947ed-132">CommonParameters</span></span>
<span data-ttu-id="947ed-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="947ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947ed-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="947ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947ed-135">입력</span><span class="sxs-lookup"><span data-stu-id="947ed-135">INPUTS</span></span>

### <span data-ttu-id="947ed-136">System.String</span><span class="sxs-lookup"><span data-stu-id="947ed-136">System.String</span></span>

### <span data-ttu-id="947ed-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="947ed-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="947ed-138">출력</span><span class="sxs-lookup"><span data-stu-id="947ed-138">OUTPUTS</span></span>

### <span data-ttu-id="947ed-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="947ed-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="947ed-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="947ed-140">NOTES</span></span>

## <span data-ttu-id="947ed-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="947ed-141">RELATED LINKS</span></span>

[<span data-ttu-id="947ed-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="947ed-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="947ed-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="947ed-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="947ed-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="947ed-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

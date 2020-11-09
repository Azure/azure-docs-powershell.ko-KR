---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309802"
---
# <span data-ttu-id="332e4-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="332e4-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="332e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="332e4-102">SYNOPSIS</span></span>
<span data-ttu-id="332e4-103">Azure Web App에 대 한 주 사이트 액세스 Restiction config의 SCM 사이트에 대 한 상속을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="332e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="332e4-104">SYNTAX</span></span>

### <span data-ttu-id="332e4-105">InputValuesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="332e4-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="332e4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="332e4-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="332e4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="332e4-107">DESCRIPTION</span></span>
<span data-ttu-id="332e4-108">**업데이트 AzWebAppAccessRestrictionConfig** Cmdlet은 Azure Web App에 대 한 액세스 제한 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="332e4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="332e4-109">EXAMPLES</span></span>

### <span data-ttu-id="332e4-110">예제 1: 웹 앱 SCM 사이트를 업데이트 하 여 기본 사이트의 액세스 제한 사용</span><span class="sxs-lookup"><span data-stu-id="332e4-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="332e4-111">다음 예제에서는 scm 사이트의 기본 사이트에 대 한 액세스 제한 구성을 사용 하도록 리소스 그룹 MyResourceGroup에 속한 IpRule 이라는 웹 앱을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="332e4-112">변수</span><span class="sxs-lookup"><span data-stu-id="332e4-112">PARAMETERS</span></span>

### <span data-ttu-id="332e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="332e4-113">-DefaultProfile</span></span>
<span data-ttu-id="332e4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="332e4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="332e4-115">-InputObject</span></span>
<span data-ttu-id="332e4-116">액세스 제한 구성 개체</span><span class="sxs-lookup"><span data-stu-id="332e4-116">The access restriction config object</span></span>

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

### <span data-ttu-id="332e4-117">-이름</span><span class="sxs-lookup"><span data-stu-id="332e4-117">-Name</span></span>
<span data-ttu-id="332e4-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="332e4-118">WebApp Name</span></span>

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

### <span data-ttu-id="332e4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="332e4-119">-PassThru</span></span>
<span data-ttu-id="332e4-120">액세스 제한 구성 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="332e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="332e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="332e4-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="332e4-122">Resource Group Name</span></span>

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

### <span data-ttu-id="332e4-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="332e4-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="332e4-124">Scm 사이트는 기본 사이트에 설정 되는 규칙을 상속 합니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="332e4-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="332e4-125">-SlotName</span></span>
<span data-ttu-id="332e4-126">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="332e4-127">-확인</span><span class="sxs-lookup"><span data-stu-id="332e4-127">-Confirm</span></span>
<span data-ttu-id="332e4-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="332e4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="332e4-129">-WhatIf</span></span>
<span data-ttu-id="332e4-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="332e4-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="332e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="332e4-132">CommonParameters</span></span>
<span data-ttu-id="332e4-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="332e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="332e4-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="332e4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="332e4-135">입력</span><span class="sxs-lookup"><span data-stu-id="332e4-135">INPUTS</span></span>

### <span data-ttu-id="332e4-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="332e4-136">System.String</span></span>

### <span data-ttu-id="332e4-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="332e4-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="332e4-138">출력</span><span class="sxs-lookup"><span data-stu-id="332e4-138">OUTPUTS</span></span>

### <span data-ttu-id="332e4-139">PSAccessRestrictionConfig를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="332e4-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="332e4-140">상속자</span><span class="sxs-lookup"><span data-stu-id="332e4-140">NOTES</span></span>

## <span data-ttu-id="332e4-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="332e4-141">RELATED LINKS</span></span>

[<span data-ttu-id="332e4-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="332e4-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="332e4-143">추가-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="332e4-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="332e4-144">제거-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="332e4-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

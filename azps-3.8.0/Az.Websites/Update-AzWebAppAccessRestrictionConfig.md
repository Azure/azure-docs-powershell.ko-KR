---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: 9069dd055fd3cccdbd1efe520fc560c385d15cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042582"
---
# <span data-ttu-id="96b8b-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="96b8b-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="96b8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="96b8b-103">Azure Web App에 대 한 주 사이트 액세스 Restiction config의 SCM 사이트에 대 한 상속을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="96b8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96b8b-104">SYNTAX</span></span>

### <span data-ttu-id="96b8b-105">InputValuesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="96b8b-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96b8b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96b8b-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96b8b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="96b8b-107">DESCRIPTION</span></span>
<span data-ttu-id="96b8b-108">**업데이트 AzWebAppAccessRestrictionConfig** Cmdlet은 Azure Web App에 대 한 액세스 제한 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="96b8b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="96b8b-109">EXAMPLES</span></span>

### <span data-ttu-id="96b8b-110">예제 1: 웹 앱 SCM 사이트를 업데이트 하 여 기본 사이트의 액세스 제한 사용</span><span class="sxs-lookup"><span data-stu-id="96b8b-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>
```
PS C:\>Set-AzWebAppAccessRestriction -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -ScmSiteUseMainSiteRestrictionConfig
```

<span data-ttu-id="96b8b-111">이 명령은 scm 사이트의 기본 사이트에 대 한 액세스 제한 구성을 사용 하도록 리소스 그룹 기본값-웹 WestUS에 속한 ContosoSite 이라는 웹 앱을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-111">This command updates a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS to use access restriction config of main site on the scm site.</span></span>

## <span data-ttu-id="96b8b-112">변수</span><span class="sxs-lookup"><span data-stu-id="96b8b-112">PARAMETERS</span></span>

### <span data-ttu-id="96b8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b8b-113">-DefaultProfile</span></span>
<span data-ttu-id="96b8b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96b8b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96b8b-115">-InputObject</span></span>
<span data-ttu-id="96b8b-116">액세스 제한 구성 개체</span><span class="sxs-lookup"><span data-stu-id="96b8b-116">The access restriction config object</span></span>

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

### <span data-ttu-id="96b8b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="96b8b-117">-Name</span></span>
<span data-ttu-id="96b8b-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="96b8b-118">WebApp Name</span></span>

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

### <span data-ttu-id="96b8b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96b8b-119">-PassThru</span></span>
<span data-ttu-id="96b8b-120">액세스 제한 구성 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="96b8b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b8b-121">-ResourceGroupName</span></span>
<span data-ttu-id="96b8b-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="96b8b-122">Resource Group Name</span></span>

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

### <span data-ttu-id="96b8b-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="96b8b-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="96b8b-124">Scm 사이트는 기본 사이트에 설정 되는 규칙을 상속 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="96b8b-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="96b8b-125">-SlotName</span></span>
<span data-ttu-id="96b8b-126">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="96b8b-127">-확인</span><span class="sxs-lookup"><span data-stu-id="96b8b-127">-Confirm</span></span>
<span data-ttu-id="96b8b-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96b8b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b8b-129">-WhatIf</span></span>
<span data-ttu-id="96b8b-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96b8b-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96b8b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b8b-132">CommonParameters</span></span>
<span data-ttu-id="96b8b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b8b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b8b-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="96b8b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b8b-135">입력</span><span class="sxs-lookup"><span data-stu-id="96b8b-135">INPUTS</span></span>

### <span data-ttu-id="96b8b-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="96b8b-136">System.String</span></span>

### <span data-ttu-id="96b8b-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="96b8b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="96b8b-138">출력</span><span class="sxs-lookup"><span data-stu-id="96b8b-138">OUTPUTS</span></span>

### <span data-ttu-id="96b8b-139">PSAccessRestrictionConfig를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="96b8b-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="96b8b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="96b8b-140">NOTES</span></span>

## <span data-ttu-id="96b8b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96b8b-141">RELATED LINKS</span></span>

[<span data-ttu-id="96b8b-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="96b8b-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="96b8b-143">추가-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="96b8b-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="96b8b-144">제거-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="96b8b-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

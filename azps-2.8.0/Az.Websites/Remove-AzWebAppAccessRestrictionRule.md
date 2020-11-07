---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874480"
---
# <span data-ttu-id="55f9d-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="55f9d-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="55f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="55f9d-103">Azure 웹 앱에서 액세스 제한 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="55f9d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55f9d-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f9d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="55f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="55f9d-106">AzWebAppAccessRestrictionRule cmdlet이 Azure 웹 앱에서 액세스 제한 규칙을 제거 **함**</span><span class="sxs-lookup"><span data-stu-id="55f9d-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="55f9d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="55f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="55f9d-108">예제 1: 웹 앱 액세스 제한 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="55f9d-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="55f9d-109">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 Azure Web App ContosoSite의 IpRule 액세스 제한 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="55f9d-110">변수</span><span class="sxs-lookup"><span data-stu-id="55f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="55f9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f9d-111">-DefaultProfile</span></span>
<span data-ttu-id="55f9d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55f9d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="55f9d-113">-Name</span></span>
<span data-ttu-id="55f9d-114">액세스 제한 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="55f9d-114">Access Restriction Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f9d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55f9d-115">-PassThru</span></span>
<span data-ttu-id="55f9d-116">액세스 제한 구성 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="55f9d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f9d-117">-ResourceGroupName</span></span>
<span data-ttu-id="55f9d-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="55f9d-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f9d-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="55f9d-119">-SlotName</span></span>
<span data-ttu-id="55f9d-120">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-120">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="55f9d-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="55f9d-121">-TargetScmSite</span></span>
<span data-ttu-id="55f9d-122">규칙은 주 사이트 또는 Scm 사이트를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="55f9d-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="55f9d-123">-WebAppName</span></span>
<span data-ttu-id="55f9d-124">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-124">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f9d-125">-확인</span><span class="sxs-lookup"><span data-stu-id="55f9d-125">-Confirm</span></span>
<span data-ttu-id="55f9d-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f9d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f9d-127">-WhatIf</span></span>
<span data-ttu-id="55f9d-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55f9d-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f9d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f9d-130">CommonParameters</span></span>
<span data-ttu-id="55f9d-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f9d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f9d-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="55f9d-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f9d-133">입력</span><span class="sxs-lookup"><span data-stu-id="55f9d-133">INPUTS</span></span>

### <span data-ttu-id="55f9d-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="55f9d-134">System.String</span></span>

## <span data-ttu-id="55f9d-135">출력</span><span class="sxs-lookup"><span data-stu-id="55f9d-135">OUTPUTS</span></span>

### <span data-ttu-id="55f9d-136">PSAccessRestrictionConfig를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="55f9d-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="55f9d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="55f9d-137">NOTES</span></span>

## <span data-ttu-id="55f9d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55f9d-138">RELATED LINKS</span></span>

[<span data-ttu-id="55f9d-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="55f9d-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="55f9d-140">업데이트-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="55f9d-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="55f9d-141">추가-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="55f9d-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

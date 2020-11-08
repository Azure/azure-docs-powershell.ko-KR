---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219254"
---
# <span data-ttu-id="3110b-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3110b-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="3110b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3110b-102">SYNOPSIS</span></span>
<span data-ttu-id="3110b-103">Azure 웹 앱에서 액세스 제한 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="3110b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3110b-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3110b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3110b-105">DESCRIPTION</span></span>
<span data-ttu-id="3110b-106">AzWebAppAccessRestrictionRule cmdlet이 Azure 웹 앱에서 액세스 제한 규칙을 제거 **함**</span><span class="sxs-lookup"><span data-stu-id="3110b-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="3110b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3110b-107">EXAMPLES</span></span>

### <span data-ttu-id="3110b-108">예제 1: 웹 앱 액세스 제한 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="3110b-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="3110b-109">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 Azure Web App ContosoSite의 IpRule 액세스 제한 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3110b-110">변수</span><span class="sxs-lookup"><span data-stu-id="3110b-110">PARAMETERS</span></span>

### <span data-ttu-id="3110b-111">-작업</span><span class="sxs-lookup"><span data-stu-id="3110b-111">-Action</span></span>
<span data-ttu-id="3110b-112">규칙 허용 또는 거부</span><span class="sxs-lookup"><span data-stu-id="3110b-112">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3110b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3110b-113">-DefaultProfile</span></span>
<span data-ttu-id="3110b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3110b-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="3110b-115">-IpAddress</span></span>
<span data-ttu-id="3110b-116">Ip 주소 v4 또는 v6 CIDR 범위</span><span class="sxs-lookup"><span data-stu-id="3110b-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="3110b-117">예: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="3110b-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="3110b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="3110b-118">-Name</span></span>
<span data-ttu-id="3110b-119">액세스 제한 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="3110b-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="3110b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3110b-120">-PassThru</span></span>
<span data-ttu-id="3110b-121">액세스 제한 구성 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="3110b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3110b-122">-ResourceGroupName</span></span>
<span data-ttu-id="3110b-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3110b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3110b-124">-SlotName</span><span class="sxs-lookup"><span data-stu-id="3110b-124">-SlotName</span></span>
<span data-ttu-id="3110b-125">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="3110b-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3110b-126">-SubnetId</span></span>
<span data-ttu-id="3110b-127">서브넷의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="3110b-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3110b-128">-SubnetName</span></span>
<span data-ttu-id="3110b-129">서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="3110b-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="3110b-130">-TargetScmSite</span></span>
<span data-ttu-id="3110b-131">규칙은 주 사이트 또는 Scm 사이트를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="3110b-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3110b-132">-VirtualNetworkName</span></span>
<span data-ttu-id="3110b-133">가상 네트워크의 이름입니다 (웹 앱과 동일한 리소스 그룹에 있어야 함).</span><span class="sxs-lookup"><span data-stu-id="3110b-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="3110b-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="3110b-134">-WebAppName</span></span>
<span data-ttu-id="3110b-135">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-135">The name of the web app.</span></span>

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

### <span data-ttu-id="3110b-136">-확인</span><span class="sxs-lookup"><span data-stu-id="3110b-136">-Confirm</span></span>
<span data-ttu-id="3110b-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3110b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3110b-138">-WhatIf</span></span>
<span data-ttu-id="3110b-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3110b-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3110b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3110b-141">CommonParameters</span></span>
<span data-ttu-id="3110b-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3110b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3110b-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3110b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3110b-144">입력</span><span class="sxs-lookup"><span data-stu-id="3110b-144">INPUTS</span></span>

### <span data-ttu-id="3110b-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3110b-145">System.String</span></span>

## <span data-ttu-id="3110b-146">출력</span><span class="sxs-lookup"><span data-stu-id="3110b-146">OUTPUTS</span></span>

### <span data-ttu-id="3110b-147">PSAccessRestrictionConfig를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="3110b-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="3110b-148">상속자</span><span class="sxs-lookup"><span data-stu-id="3110b-148">NOTES</span></span>

## <span data-ttu-id="3110b-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3110b-149">RELATED LINKS</span></span>

[<span data-ttu-id="3110b-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3110b-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3110b-151">업데이트-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3110b-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3110b-152">추가-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3110b-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

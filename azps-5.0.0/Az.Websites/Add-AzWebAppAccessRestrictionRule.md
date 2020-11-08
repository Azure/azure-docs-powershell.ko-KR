---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0abad2b3d38a5f614222a8eda7e3c27b9fda9556
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216494"
---
# <span data-ttu-id="e43d0-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="e43d0-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="e43d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e43d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e43d0-103">Azure Web App에 Access Restiction 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="e43d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e43d0-104">SYNTAX</span></span>

### <span data-ttu-id="e43d0-105">IpAddressParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e43d0-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e43d0-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e43d0-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e43d0-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e43d0-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e43d0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e43d0-108">DESCRIPTION</span></span>
<span data-ttu-id="e43d0-109">**Add-AzWebAppAccessRestrictionRule** Cmdlet은 Azure 웹 앱에 액세스 제한 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="e43d0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e43d0-110">EXAMPLES</span></span>

### <span data-ttu-id="e43d0-111">예제 1: 웹 앱에 IpAddress 액세스 제한 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="e43d0-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="e43d0-112">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 ContosoSite 이라는 웹 앱에 우선 순위 200 및 ip 범위에 대 한 액세스 제한 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="e43d0-113">예제 2: 웹 앱에 서브넷 서비스 끝점 액세스 제한 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="e43d0-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="e43d0-114">이 명령은 appgw에 우선 순위 300를 사용 하는 액세스 제한 규칙을 추가 하 고, corp-vnet의 서브넷-subnet에는 리소스 그룹 기본값-웹 WestUS에 속하는 ContosoSite 라는 웹 앱에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e43d0-115">변수</span><span class="sxs-lookup"><span data-stu-id="e43d0-115">PARAMETERS</span></span>

### <span data-ttu-id="e43d0-116">-작업</span><span class="sxs-lookup"><span data-stu-id="e43d0-116">-Action</span></span>
<span data-ttu-id="e43d0-117">규칙 허용 또는 거부</span><span class="sxs-lookup"><span data-stu-id="e43d0-117">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="e43d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43d0-118">-DefaultProfile</span></span>
<span data-ttu-id="e43d0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43d0-120">-설명</span><span class="sxs-lookup"><span data-stu-id="e43d0-120">-Description</span></span>
<span data-ttu-id="e43d0-121">액세스 제한 설명.</span><span class="sxs-lookup"><span data-stu-id="e43d0-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="e43d0-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e43d0-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="e43d0-123">서브넷에서 서비스 끝점 등록의 유효성을 검사할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43d0-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="e43d0-124">-IpAddress</span></span>
<span data-ttu-id="e43d0-125">Ip 주소 v4 또는 v6 CIDR 범위</span><span class="sxs-lookup"><span data-stu-id="e43d0-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="e43d0-126">예: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="e43d0-126">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43d0-127">-이름</span><span class="sxs-lookup"><span data-stu-id="e43d0-127">-Name</span></span>
<span data-ttu-id="e43d0-128">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="e43d0-128">Rule Name</span></span>

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

### <span data-ttu-id="e43d0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e43d0-129">-PassThru</span></span>
<span data-ttu-id="e43d0-130">액세스 제한 구성 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="e43d0-131">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="e43d0-131">-Priority</span></span>
<span data-ttu-id="e43d0-132">액세스 제한 우선 순위.</span><span class="sxs-lookup"><span data-stu-id="e43d0-132">Access Restriction priority.</span></span> <span data-ttu-id="e43d0-133">예: 500.</span><span class="sxs-lookup"><span data-stu-id="e43d0-133">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43d0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43d0-134">-ResourceGroupName</span></span>
<span data-ttu-id="e43d0-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e43d0-135">Resource Group Name</span></span>

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

### <span data-ttu-id="e43d0-136">-SlotName</span><span class="sxs-lookup"><span data-stu-id="e43d0-136">-SlotName</span></span>
<span data-ttu-id="e43d0-137">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="e43d0-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e43d0-138">-SubnetId</span></span>
<span data-ttu-id="e43d0-139">서브넷의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-139">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43d0-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e43d0-140">-SubnetName</span></span>
<span data-ttu-id="e43d0-141">서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-141">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43d0-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="e43d0-142">-TargetScmSite</span></span>
<span data-ttu-id="e43d0-143">규칙은 주 사이트 또는 Scm 사이트를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="e43d0-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e43d0-144">-VirtualNetworkName</span></span>
<span data-ttu-id="e43d0-145">가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-145">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43d0-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e43d0-146">-WebAppName</span></span>
<span data-ttu-id="e43d0-147">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-147">The name of the web app.</span></span>

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

### <span data-ttu-id="e43d0-148">-확인</span><span class="sxs-lookup"><span data-stu-id="e43d0-148">-Confirm</span></span>
<span data-ttu-id="e43d0-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e43d0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e43d0-150">-WhatIf</span></span>
<span data-ttu-id="e43d0-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e43d0-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e43d0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43d0-153">CommonParameters</span></span>
<span data-ttu-id="e43d0-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43d0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43d0-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e43d0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43d0-156">입력</span><span class="sxs-lookup"><span data-stu-id="e43d0-156">INPUTS</span></span>

### <span data-ttu-id="e43d0-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e43d0-157">System.String</span></span>

## <span data-ttu-id="e43d0-158">출력</span><span class="sxs-lookup"><span data-stu-id="e43d0-158">OUTPUTS</span></span>

### <span data-ttu-id="e43d0-159">PSAccessRestrictionConfig를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="e43d0-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="e43d0-160">상속자</span><span class="sxs-lookup"><span data-stu-id="e43d0-160">NOTES</span></span>

## <span data-ttu-id="e43d0-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e43d0-161">RELATED LINKS</span></span>

[<span data-ttu-id="e43d0-162">업데이트-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="e43d0-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="e43d0-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="e43d0-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="e43d0-164">제거-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="e43d0-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

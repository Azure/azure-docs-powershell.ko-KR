---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 03f898246b2f0d784725488f753697ed893b09df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015403"
---
# <span data-ttu-id="af8fb-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="af8fb-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="af8fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="af8fb-103">가상 머신에 AD 도메인 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="af8fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="af8fb-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af8fb-105">설명</span><span class="sxs-lookup"><span data-stu-id="af8fb-105">DESCRIPTION</span></span>
<span data-ttu-id="af8fb-106">**Set-AzVMADomainExtension** cmdlet은 가상 머신에 AD(Azure Active Directory) 도메인 가상 머신 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="af8fb-107">이 확장을 사용하면 가상 머신이 도메인에 조인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="af8fb-108">예제</span><span class="sxs-lookup"><span data-stu-id="af8fb-108">EXAMPLES</span></span>

## <span data-ttu-id="af8fb-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="af8fb-109">PARAMETERS</span></span>

### <span data-ttu-id="af8fb-110">-자격 증명</span><span class="sxs-lookup"><span data-stu-id="af8fb-110">-Credential</span></span>
<span data-ttu-id="af8fb-111">가상 머신에 대한 사용자 이름 및 암호를 **PSCredential 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="af8fb-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="af8fb-112">자격 증명을 얻은 경우 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="af8fb-113">자세한 내용은 `Get-Help Get-Credential` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af8fb-114">-DefaultProfile</span></span>
<span data-ttu-id="af8fb-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af8fb-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="af8fb-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="af8fb-117">이 cmdlet은 확장의 부 버전 자동 업그레이드를 사용하지 않도록 설정하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="af8fb-118">-DomainName</span></span>
<span data-ttu-id="af8fb-119">도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="af8fb-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="af8fb-120">-ForceRerun</span></span>
<span data-ttu-id="af8fb-121">이 cmdlet은 확장을 삭제하고 다시 설치하지 않고 가상 머신에서 동일한 확장 구성을 다시 억지합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="af8fb-122">값은 현재 값과 다른 문자열일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="af8fb-123">forceUpdateTag가 변경되지 않은 경우 처리기에서 공용 또는 보호된 설정에 대한 업데이트가 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="af8fb-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="af8fb-124">-JoinOption</span></span>
<span data-ttu-id="af8fb-125">조인 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-125">Specifies the join option.</span></span> <span data-ttu-id="af8fb-126">조인 옵션은 [fJoinOptions를 참조하세요.](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="af8fb-126">For join options see [fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-127">-Location</span><span class="sxs-lookup"><span data-stu-id="af8fb-127">-Location</span></span>
<span data-ttu-id="af8fb-128">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="af8fb-129">-Name</span><span class="sxs-lookup"><span data-stu-id="af8fb-129">-Name</span></span>
<span data-ttu-id="af8fb-130">추가할 도메인 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-130">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="af8fb-131">-NoWait</span></span>
<span data-ttu-id="af8fb-132">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="af8fb-133">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="af8fb-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="af8fb-134">-OUPath</span></span>
<span data-ttu-id="af8fb-135">도메인 계정에 대한 조직 단위(OU)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="af8fb-136">OU의 전체 고유 이름을 인용 부호에 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="af8fb-137">기본값은 도메인의 컴퓨터 개체에 대한 기본 OU입니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="af8fb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af8fb-138">-ResourceGroupName</span></span>
<span data-ttu-id="af8fb-139">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="af8fb-140">-다시 시작</span><span class="sxs-lookup"><span data-stu-id="af8fb-140">-Restart</span></span>
<span data-ttu-id="af8fb-141">이 cmdlet이 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="af8fb-142">변경을 효과적으로 실행하려면 다시 시작해야 하는 경우가 종종 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-142">A restart is often required to make the change effective.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="af8fb-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="af8fb-144">도메인 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-144">Specifies the version of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="af8fb-145">-VMName</span></span>
<span data-ttu-id="af8fb-146">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-146">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-147">-확인</span><span class="sxs-lookup"><span data-stu-id="af8fb-147">-Confirm</span></span>
<span data-ttu-id="af8fb-148">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af8fb-149">-WhatIf</span></span>
<span data-ttu-id="af8fb-150">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af8fb-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8fb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af8fb-152">CommonParameters</span></span>
<span data-ttu-id="af8fb-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af8fb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af8fb-154">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af8fb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af8fb-155">입력</span><span class="sxs-lookup"><span data-stu-id="af8fb-155">INPUTS</span></span>

### <span data-ttu-id="af8fb-156">System.String</span><span class="sxs-lookup"><span data-stu-id="af8fb-156">System.String</span></span>

### <span data-ttu-id="af8fb-157">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af8fb-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af8fb-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="af8fb-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="af8fb-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af8fb-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af8fb-160">출력</span><span class="sxs-lookup"><span data-stu-id="af8fb-160">OUTPUTS</span></span>

### <span data-ttu-id="af8fb-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="af8fb-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="af8fb-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af8fb-162">NOTES</span></span>

## <span data-ttu-id="af8fb-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af8fb-163">RELATED LINKS</span></span>

[<span data-ttu-id="af8fb-164">Get-AzVMADomainExtension</span><span class="sxs-lookup"><span data-stu-id="af8fb-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)

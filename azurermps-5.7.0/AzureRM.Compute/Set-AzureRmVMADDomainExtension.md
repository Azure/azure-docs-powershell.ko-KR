---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525276"
---
# <span data-ttu-id="8daf8-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8daf8-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="8daf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8daf8-102">SYNOPSIS</span></span>
<span data-ttu-id="8daf8-103">가상 컴퓨터에 AD 도메인 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8daf8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8daf8-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8daf8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8daf8-105">DESCRIPTION</span></span>
<span data-ttu-id="8daf8-106">**AzureRmVMADDomainExtension** cmdlet은 가상 컴퓨터에 Azure AD (Active Directory) 도메인 가상 컴퓨터 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="8daf8-107">이 확장을 통해 가상 컴퓨터가 도메인에 가입할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="8daf8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8daf8-108">EXAMPLES</span></span>

## <span data-ttu-id="8daf8-109">변수</span><span class="sxs-lookup"><span data-stu-id="8daf8-109">PARAMETERS</span></span>

### <span data-ttu-id="8daf8-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="8daf8-110">-Credential</span></span>
<span data-ttu-id="8daf8-111">가상 컴퓨터에 대 한 사용자 이름 및 암호를 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="8daf8-112">자격 증명을 얻으려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="8daf8-113">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="8daf8-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8daf8-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8daf8-115">이 cmdlet이 확장의 부 버전에 대 한 자동 업그레이드를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-116">-DomainName</span><span class="sxs-lookup"><span data-stu-id="8daf8-116">-DomainName</span></span>
<span data-ttu-id="8daf8-117">도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-117">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="8daf8-118">-ForceRerun</span></span>
<span data-ttu-id="8daf8-119">이 cmdlet이 확장을 제거 하 고 다시 설치 하지 않고 가상 컴퓨터에서 동일한 확장 구성을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="8daf8-120">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="8daf8-121">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="8daf8-122">-JoinOption</span></span>
<span data-ttu-id="8daf8-123">조인 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-123">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-124">-위치</span><span class="sxs-lookup"><span data-stu-id="8daf8-124">-Location</span></span>
<span data-ttu-id="8daf8-125">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-126">-이름</span><span class="sxs-lookup"><span data-stu-id="8daf8-126">-Name</span></span>
<span data-ttu-id="8daf8-127">추가할 도메인 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-127">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="8daf8-128">-OUPath</span></span>
<span data-ttu-id="8daf8-129">도메인 계정에 대 한 OU (조직 구성 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="8daf8-130">OU의 전체 고유 이름을 따옴표로 묶어 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="8daf8-131">기본 값은 도메인의 컴퓨터 개체에 대 한 기본 OU입니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-131">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8daf8-132">-ResourceGroupName</span></span>
<span data-ttu-id="8daf8-133">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-133">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-134">-다시 시작</span><span class="sxs-lookup"><span data-stu-id="8daf8-134">-Restart</span></span>
<span data-ttu-id="8daf8-135">이 cmdlet이 가상 컴퓨터를 다시 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="8daf8-136">변경 사항을 적용 하려면 일반적으로 시스템을 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-136">A restart is often required to make the change effective.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8daf8-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="8daf8-138">도메인 확장명의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-138">Specifies the version of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="8daf8-139">-VMName</span></span>
<span data-ttu-id="8daf8-140">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-140">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-141">-확인</span><span class="sxs-lookup"><span data-stu-id="8daf8-141">-Confirm</span></span>
<span data-ttu-id="8daf8-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8daf8-143">-WhatIf</span></span>
<span data-ttu-id="8daf8-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8daf8-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8daf8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8daf8-146">CommonParameters</span></span>
<span data-ttu-id="8daf8-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8daf8-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8daf8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8daf8-149">입력</span><span class="sxs-lookup"><span data-stu-id="8daf8-149">INPUTS</span></span>

### <span data-ttu-id="8daf8-150">않아야</span><span class="sxs-lookup"><span data-stu-id="8daf8-150">None</span></span>
<span data-ttu-id="8daf8-151">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8daf8-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8daf8-152">출력</span><span class="sxs-lookup"><span data-stu-id="8daf8-152">OUTPUTS</span></span>

## <span data-ttu-id="8daf8-153">상속자</span><span class="sxs-lookup"><span data-stu-id="8daf8-153">NOTES</span></span>

## <span data-ttu-id="8daf8-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8daf8-154">RELATED LINKS</span></span>

[<span data-ttu-id="8daf8-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8daf8-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)

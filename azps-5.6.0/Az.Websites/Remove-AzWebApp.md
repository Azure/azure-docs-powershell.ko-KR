---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 1ce172ea2f1851f2f75a95a3037798ca3b3a2bf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961067"
---
# <span data-ttu-id="0c065-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c065-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="0c065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c065-102">SYNOPSIS</span></span>
<span data-ttu-id="0c065-103">Azure Web App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="0c065-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c065-104">SYNTAX</span></span>

### <span data-ttu-id="0c065-105">S1</span><span class="sxs-lookup"><span data-stu-id="0c065-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c065-106">S2</span><span class="sxs-lookup"><span data-stu-id="0c065-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c065-107">설명</span><span class="sxs-lookup"><span data-stu-id="0c065-107">DESCRIPTION</span></span>
<span data-ttu-id="0c065-108">**Remove-AzWebApp** cmdlet은 리소스 그룹 및 웹앱 이름을 제공한 Azure Web App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="0c065-109">이 cmdlet은 기본적으로 모든 슬롯 및 메트릭도 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="0c065-110">예제</span><span class="sxs-lookup"><span data-stu-id="0c065-110">EXAMPLES</span></span>

### <span data-ttu-id="0c065-111">예제 1: 웹앱 제거</span><span class="sxs-lookup"><span data-stu-id="0c065-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="0c065-112">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoSite라는 Azure Web App을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0c065-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0c065-113">PARAMETERS</span></span>

### <span data-ttu-id="0c065-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c065-114">-AsJob</span></span>
<span data-ttu-id="0c065-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0c065-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c065-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c065-116">-DefaultProfile</span></span>
<span data-ttu-id="0c065-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c065-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0c065-118">-Force</span></span>
<span data-ttu-id="0c065-119">강제 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="0c065-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="0c065-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0c065-120">-Name</span></span>
<span data-ttu-id="0c065-121">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="0c065-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c065-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c065-122">-ResourceGroupName</span></span>
<span data-ttu-id="0c065-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0c065-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c065-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0c065-124">-WebApp</span></span>
<span data-ttu-id="0c065-125">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="0c065-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c065-126">-확인</span><span class="sxs-lookup"><span data-stu-id="0c065-126">-Confirm</span></span>
<span data-ttu-id="0c065-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다. cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c065-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c065-128">-WhatIf</span></span>
<span data-ttu-id="0c065-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c065-130">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c065-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c065-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c065-132">CommonParameters</span></span>
<span data-ttu-id="0c065-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c065-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c065-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0c065-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c065-135">입력</span><span class="sxs-lookup"><span data-stu-id="0c065-135">INPUTS</span></span>

### <span data-ttu-id="0c065-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0c065-136">System.String</span></span>

### <span data-ttu-id="0c065-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0c065-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0c065-138">출력</span><span class="sxs-lookup"><span data-stu-id="0c065-138">OUTPUTS</span></span>

### <span data-ttu-id="0c065-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="0c065-139">System.Void</span></span>

## <span data-ttu-id="0c065-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c065-140">NOTES</span></span>

## <span data-ttu-id="0c065-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c065-141">RELATED LINKS</span></span>

[<span data-ttu-id="0c065-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c065-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0c065-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c065-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0c065-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c065-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0c065-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c065-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0c065-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c065-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



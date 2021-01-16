---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326157"
---
# <span data-ttu-id="50967-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50967-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="50967-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50967-102">SYNOPSIS</span></span>
<span data-ttu-id="50967-103">Azure 웹앱을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50967-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="50967-104">구문</span><span class="sxs-lookup"><span data-stu-id="50967-104">SYNTAX</span></span>

### <span data-ttu-id="50967-105">S1</span><span class="sxs-lookup"><span data-stu-id="50967-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50967-106">S2</span><span class="sxs-lookup"><span data-stu-id="50967-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50967-107">설명</span><span class="sxs-lookup"><span data-stu-id="50967-107">DESCRIPTION</span></span>
<span data-ttu-id="50967-108">**Remove-AzWebApp** cmdlet은 리소스 그룹 및 웹앱 이름을 제공한 Azure 웹앱을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50967-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="50967-109">이 cmdlet은 기본적으로 모든 슬롯 및 메트릭도 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50967-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="50967-110">예제</span><span class="sxs-lookup"><span data-stu-id="50967-110">EXAMPLES</span></span>

### <span data-ttu-id="50967-111">예제 1: 웹앱 제거</span><span class="sxs-lookup"><span data-stu-id="50967-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="50967-112">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoSite라는 Azure 웹앱을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50967-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="50967-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50967-113">PARAMETERS</span></span>

### <span data-ttu-id="50967-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50967-114">-AsJob</span></span>
<span data-ttu-id="50967-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="50967-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50967-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50967-116">-DefaultProfile</span></span>
<span data-ttu-id="50967-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50967-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50967-118">-Force</span><span class="sxs-lookup"><span data-stu-id="50967-118">-Force</span></span>
<span data-ttu-id="50967-119">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="50967-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="50967-120">-Name</span><span class="sxs-lookup"><span data-stu-id="50967-120">-Name</span></span>
<span data-ttu-id="50967-121">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="50967-121">WebApp Name</span></span>

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

### <span data-ttu-id="50967-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50967-122">-ResourceGroupName</span></span>
<span data-ttu-id="50967-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="50967-123">Resource Group Name</span></span>

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

### <span data-ttu-id="50967-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="50967-124">-WebApp</span></span>
<span data-ttu-id="50967-125">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="50967-125">WebApp Object</span></span>

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

### <span data-ttu-id="50967-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50967-126">-Confirm</span></span>
<span data-ttu-id="50967-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다. cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50967-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50967-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50967-128">-WhatIf</span></span>
<span data-ttu-id="50967-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="50967-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50967-130">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="50967-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50967-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50967-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50967-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50967-132">CommonParameters</span></span>
<span data-ttu-id="50967-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50967-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50967-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="50967-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50967-135">입력</span><span class="sxs-lookup"><span data-stu-id="50967-135">INPUTS</span></span>

### <span data-ttu-id="50967-136">System.String</span><span class="sxs-lookup"><span data-stu-id="50967-136">System.String</span></span>

### <span data-ttu-id="50967-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="50967-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="50967-138">출력</span><span class="sxs-lookup"><span data-stu-id="50967-138">OUTPUTS</span></span>

### <span data-ttu-id="50967-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="50967-139">System.Void</span></span>

## <span data-ttu-id="50967-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50967-140">NOTES</span></span>

## <span data-ttu-id="50967-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50967-141">RELATED LINKS</span></span>

[<span data-ttu-id="50967-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50967-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="50967-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50967-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="50967-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50967-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="50967-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50967-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="50967-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="50967-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



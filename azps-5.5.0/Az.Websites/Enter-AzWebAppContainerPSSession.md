---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182497"
---
# <span data-ttu-id="f6e61-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="f6e61-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="f6e61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6e61-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e61-103">지정된 사이트 또는 슬롯 및 지정된 리소스 그룹에 지정된 Windows 컨테이너에 원격 PowerShell 세션을 여는 경우</span><span class="sxs-lookup"><span data-stu-id="f6e61-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="f6e61-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6e61-104">SYNTAX</span></span>

### <span data-ttu-id="f6e61-105">S1(기본값)</span><span class="sxs-lookup"><span data-stu-id="f6e61-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6e61-106">S2</span><span class="sxs-lookup"><span data-stu-id="f6e61-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6e61-107">설명</span><span class="sxs-lookup"><span data-stu-id="f6e61-107">DESCRIPTION</span></span>
<span data-ttu-id="f6e61-108">지정된 사이트 또는 슬롯 및 지정된 리소스 그룹에 지정된 Windows 컨테이너에 원격 PowerShell 세션을 여는 경우</span><span class="sxs-lookup"><span data-stu-id="f6e61-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="f6e61-109">예제</span><span class="sxs-lookup"><span data-stu-id="f6e61-109">EXAMPLES</span></span>

### <span data-ttu-id="f6e61-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f6e61-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="f6e61-111">이 명령은 Windows 컨테이너 앱 ContosoASP에 원격 PowerShell 세션을 여는 경우</span><span class="sxs-lookup"><span data-stu-id="f6e61-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="f6e61-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6e61-112">PARAMETERS</span></span>

### <span data-ttu-id="f6e61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e61-113">-DefaultProfile</span></span>
<span data-ttu-id="f6e61-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e61-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f6e61-115">-Force</span></span>
<span data-ttu-id="f6e61-116">확인 메시지를 표시하지 않고 PowerShell 세션을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f6e61-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f6e61-117">-Name</span></span>
<span data-ttu-id="f6e61-118">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-118">The name of the web app.</span></span>

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

### <span data-ttu-id="f6e61-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6e61-119">-PassThru</span></span>
<span data-ttu-id="f6e61-120">성공 또는 실패를 나타내는 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="f6e61-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e61-121">-ResourceGroupName</span></span>
<span data-ttu-id="f6e61-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6e61-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="f6e61-123">-SlotName</span></span>
<span data-ttu-id="f6e61-124">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e61-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f6e61-125">-WebApp</span></span>
<span data-ttu-id="f6e61-126">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="f6e61-126">The web app object</span></span>

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

### <span data-ttu-id="f6e61-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6e61-127">-Confirm</span></span>
<span data-ttu-id="f6e61-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6e61-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6e61-129">-WhatIf</span></span>
<span data-ttu-id="f6e61-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f6e61-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6e61-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6e61-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e61-132">CommonParameters</span></span>
<span data-ttu-id="f6e61-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e61-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e61-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f6e61-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e61-135">입력</span><span class="sxs-lookup"><span data-stu-id="f6e61-135">INPUTS</span></span>

### <span data-ttu-id="f6e61-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f6e61-136">System.String</span></span>

### <span data-ttu-id="f6e61-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f6e61-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f6e61-138">출력</span><span class="sxs-lookup"><span data-stu-id="f6e61-138">OUTPUTS</span></span>

### <span data-ttu-id="f6e61-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="f6e61-139">System.Void</span></span>

## <span data-ttu-id="f6e61-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6e61-140">NOTES</span></span>

## <span data-ttu-id="f6e61-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6e61-141">RELATED LINKS</span></span>

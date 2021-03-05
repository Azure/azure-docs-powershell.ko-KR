---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: e889e3f8d3d94993494c10141629eee6dceed01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972384"
---
# <span data-ttu-id="ead71-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="ead71-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="ead71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ead71-102">SYNOPSIS</span></span>
<span data-ttu-id="ead71-103">지정된 사이트 또는 슬롯 및 지정된 리소스 그룹에 지정된 Windows 컨테이너에 원격 PowerShell 세션 열기</span><span class="sxs-lookup"><span data-stu-id="ead71-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ead71-104">구문</span><span class="sxs-lookup"><span data-stu-id="ead71-104">SYNTAX</span></span>

### <span data-ttu-id="ead71-105">S1(기본값)</span><span class="sxs-lookup"><span data-stu-id="ead71-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead71-106">S2</span><span class="sxs-lookup"><span data-stu-id="ead71-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead71-107">설명</span><span class="sxs-lookup"><span data-stu-id="ead71-107">DESCRIPTION</span></span>
<span data-ttu-id="ead71-108">지정된 사이트 또는 슬롯 및 지정된 리소스 그룹에 지정된 Windows 컨테이너로 원격 PowerShell 세션을 니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ead71-109">예제</span><span class="sxs-lookup"><span data-stu-id="ead71-109">EXAMPLES</span></span>

### <span data-ttu-id="ead71-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ead71-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ead71-111">이 명령은 원격 PowerShell 세션을 Windows 컨테이너 앱 ContosoASP로 열립니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="ead71-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ead71-112">PARAMETERS</span></span>

### <span data-ttu-id="ead71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead71-113">-DefaultProfile</span></span>
<span data-ttu-id="ead71-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead71-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ead71-115">-Force</span></span>
<span data-ttu-id="ead71-116">확인을 요청하지 않고 PowerShell 세션을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ead71-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ead71-117">-Name</span></span>
<span data-ttu-id="ead71-118">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-118">The name of the web app.</span></span>

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

### <span data-ttu-id="ead71-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ead71-119">-PassThru</span></span>
<span data-ttu-id="ead71-120">성공 또는 실패를 나타내는 값 반환</span><span class="sxs-lookup"><span data-stu-id="ead71-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="ead71-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead71-121">-ResourceGroupName</span></span>
<span data-ttu-id="ead71-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ead71-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ead71-123">-SlotName</span></span>
<span data-ttu-id="ead71-124">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="ead71-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ead71-125">-WebApp</span></span>
<span data-ttu-id="ead71-126">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="ead71-126">The web app object</span></span>

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

### <span data-ttu-id="ead71-127">-확인</span><span class="sxs-lookup"><span data-stu-id="ead71-127">-Confirm</span></span>
<span data-ttu-id="ead71-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead71-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead71-129">-WhatIf</span></span>
<span data-ttu-id="ead71-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ead71-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead71-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead71-132">CommonParameters</span></span>
<span data-ttu-id="ead71-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ead71-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead71-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ead71-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead71-135">입력</span><span class="sxs-lookup"><span data-stu-id="ead71-135">INPUTS</span></span>

### <span data-ttu-id="ead71-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ead71-136">System.String</span></span>

### <span data-ttu-id="ead71-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ead71-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ead71-138">출력</span><span class="sxs-lookup"><span data-stu-id="ead71-138">OUTPUTS</span></span>

### <span data-ttu-id="ead71-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="ead71-139">System.Void</span></span>

## <span data-ttu-id="ead71-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ead71-140">NOTES</span></span>

## <span data-ttu-id="ead71-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ead71-141">RELATED LINKS</span></span>

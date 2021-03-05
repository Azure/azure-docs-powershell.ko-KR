---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 213fbd5e035c48892db1c44fb4ac8de8fbf8bba9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967120"
---
# <span data-ttu-id="efaa3-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="efaa3-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="efaa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="efaa3-103">New-AzWebAppContainerPSSession 사이트 또는 슬롯 및 지정된 리소스 그룹에 지정된 windows 컨테이너에 새 원격 PowerShell 세션을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="efaa3-104">구문</span><span class="sxs-lookup"><span data-stu-id="efaa3-104">SYNTAX</span></span>

### <span data-ttu-id="efaa3-105">S1(기본값)</span><span class="sxs-lookup"><span data-stu-id="efaa3-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efaa3-106">S2</span><span class="sxs-lookup"><span data-stu-id="efaa3-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efaa3-107">설명</span><span class="sxs-lookup"><span data-stu-id="efaa3-107">DESCRIPTION</span></span>
<span data-ttu-id="efaa3-108">New-AzWebAppContainerPSSession 사이트 또는 슬롯 및 지정된 리소스 그룹에 지정된 windows 컨테이너에 새 원격 PowerShell 세션을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="efaa3-109">예제</span><span class="sxs-lookup"><span data-stu-id="efaa3-109">EXAMPLES</span></span>

### <span data-ttu-id="efaa3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="efaa3-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="efaa3-111">이렇게 하면 Windows 컨테이너 앱 ContosoASP에 새 원격 PowerShell 세션이 생성되고 컨테이너 ContosoASP에서 실행 중인 프로세스를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="efaa3-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="efaa3-112">PARAMETERS</span></span>

### <span data-ttu-id="efaa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efaa3-113">-DefaultProfile</span></span>
<span data-ttu-id="efaa3-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efaa3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="efaa3-115">-Force</span></span>
<span data-ttu-id="efaa3-116">확인을 요청하지 않고 PowerShell 세션을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="efaa3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="efaa3-117">-Name</span></span>
<span data-ttu-id="efaa3-118">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-118">The name of the web app.</span></span>

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

### <span data-ttu-id="efaa3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efaa3-119">-ResourceGroupName</span></span>
<span data-ttu-id="efaa3-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="efaa3-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="efaa3-121">-SlotName</span></span>
<span data-ttu-id="efaa3-122">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="efaa3-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="efaa3-123">-WebApp</span></span>
<span data-ttu-id="efaa3-124">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="efaa3-124">The web app object</span></span>

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

### <span data-ttu-id="efaa3-125">-확인</span><span class="sxs-lookup"><span data-stu-id="efaa3-125">-Confirm</span></span>
<span data-ttu-id="efaa3-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efaa3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efaa3-127">-WhatIf</span></span>
<span data-ttu-id="efaa3-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efaa3-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efaa3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efaa3-130">CommonParameters</span></span>
<span data-ttu-id="efaa3-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efaa3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efaa3-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="efaa3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efaa3-133">입력</span><span class="sxs-lookup"><span data-stu-id="efaa3-133">INPUTS</span></span>

### <span data-ttu-id="efaa3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="efaa3-134">System.String</span></span>

### <span data-ttu-id="efaa3-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="efaa3-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="efaa3-136">출력</span><span class="sxs-lookup"><span data-stu-id="efaa3-136">OUTPUTS</span></span>

### <span data-ttu-id="efaa3-137">System.Management.Automation.Runspaces.PSSession</span><span class="sxs-lookup"><span data-stu-id="efaa3-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="efaa3-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efaa3-138">NOTES</span></span>

## <span data-ttu-id="efaa3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efaa3-139">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 651ca91a8da5a025040127b4e3bbcedf16225faf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871421"
---
# <span data-ttu-id="0219e-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="0219e-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="0219e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0219e-102">SYNOPSIS</span></span>
<span data-ttu-id="0219e-103">New-AzWebAppContainerPSSession는 지정 된 사이트 또는 슬롯 및 지정 된 리소스 그룹에서 지정한 windows 컨테이너에 새 원격 PowerShell 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="0219e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0219e-104">SYNTAX</span></span>

### <span data-ttu-id="0219e-105">S1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0219e-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0219e-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="0219e-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0219e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0219e-107">DESCRIPTION</span></span>
<span data-ttu-id="0219e-108">New-AzWebAppContainerPSSession는 지정 된 사이트 또는 슬롯 및 지정 된 리소스 그룹에서 지정한 windows 컨테이너에 새 원격 PowerShell 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="0219e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0219e-109">EXAMPLES</span></span>

### <span data-ttu-id="0219e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0219e-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="0219e-111">이렇게 하면 windows 컨테이너 앱 ContosoASP에 새 원격 PowerShell 세션이 생성 되 고 컨테이너에서 실행 중인 프로세스가 표시 됩니다 ContosoASP</span><span class="sxs-lookup"><span data-stu-id="0219e-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="0219e-112">변수</span><span class="sxs-lookup"><span data-stu-id="0219e-112">PARAMETERS</span></span>

### <span data-ttu-id="0219e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0219e-113">-DefaultProfile</span></span>
<span data-ttu-id="0219e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0219e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0219e-115">-Force</span></span>
<span data-ttu-id="0219e-116">확인 메시지를 표시 하지 않고 PowerShell 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0219e-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0219e-117">-Name</span></span>
<span data-ttu-id="0219e-118">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-118">The name of the web app.</span></span>

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

### <span data-ttu-id="0219e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0219e-119">-ResourceGroupName</span></span>
<span data-ttu-id="0219e-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="0219e-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="0219e-121">-SlotName</span></span>
<span data-ttu-id="0219e-122">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="0219e-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="0219e-123">-WebApp</span></span>
<span data-ttu-id="0219e-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="0219e-124">The web app object</span></span>

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

### <span data-ttu-id="0219e-125">-확인</span><span class="sxs-lookup"><span data-stu-id="0219e-125">-Confirm</span></span>
<span data-ttu-id="0219e-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0219e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0219e-127">-WhatIf</span></span>
<span data-ttu-id="0219e-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0219e-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0219e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0219e-130">CommonParameters</span></span>
<span data-ttu-id="0219e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0219e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0219e-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0219e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0219e-133">입력</span><span class="sxs-lookup"><span data-stu-id="0219e-133">INPUTS</span></span>

### <span data-ttu-id="0219e-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0219e-134">System.String</span></span>

### <span data-ttu-id="0219e-135">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="0219e-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0219e-136">출력</span><span class="sxs-lookup"><span data-stu-id="0219e-136">OUTPUTS</span></span>

### <span data-ttu-id="0219e-137">Runspaces-Management</span><span class="sxs-lookup"><span data-stu-id="0219e-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="0219e-138">상속자</span><span class="sxs-lookup"><span data-stu-id="0219e-138">NOTES</span></span>

## <span data-ttu-id="0219e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0219e-139">RELATED LINKS</span></span>

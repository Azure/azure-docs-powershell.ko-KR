---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213140"
---
# <span data-ttu-id="a69f6-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="a69f6-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="a69f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a69f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a69f6-103">지정한 사이트 또는 슬롯에 지정 된 windows 컨테이너 및 지정 된 리소스 그룹에 원격 PowerShell 세션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="a69f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a69f6-104">SYNTAX</span></span>

### <span data-ttu-id="a69f6-105">S1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a69f6-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a69f6-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="a69f6-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a69f6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a69f6-107">DESCRIPTION</span></span>
<span data-ttu-id="a69f6-108">지정한 사이트 또는 슬롯에 지정 된 windows 컨테이너 및 지정 된 리소스 그룹에 원격 PowerShell 세션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="a69f6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a69f6-109">EXAMPLES</span></span>

### <span data-ttu-id="a69f6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a69f6-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="a69f6-111">이 명령은 windows 컨테이너 앱 ContosoASP에 대 한 원격 PowerShell 세션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="a69f6-112">변수</span><span class="sxs-lookup"><span data-stu-id="a69f6-112">PARAMETERS</span></span>

### <span data-ttu-id="a69f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69f6-113">-DefaultProfile</span></span>
<span data-ttu-id="a69f6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a69f6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a69f6-115">-Force</span></span>
<span data-ttu-id="a69f6-116">확인 메시지를 표시 하지 않고 PowerShell 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a69f6-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a69f6-117">-Name</span></span>
<span data-ttu-id="a69f6-118">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-118">The name of the web app.</span></span>

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

### <span data-ttu-id="a69f6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a69f6-119">-PassThru</span></span>
<span data-ttu-id="a69f6-120">성공 또는 실패를 나타내는 값 반환</span><span class="sxs-lookup"><span data-stu-id="a69f6-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="a69f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="a69f6-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a69f6-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a69f6-123">-SlotName</span></span>
<span data-ttu-id="a69f6-124">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a69f6-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="a69f6-125">-WebApp</span></span>
<span data-ttu-id="a69f6-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="a69f6-126">The web app object</span></span>

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

### <span data-ttu-id="a69f6-127">-확인</span><span class="sxs-lookup"><span data-stu-id="a69f6-127">-Confirm</span></span>
<span data-ttu-id="a69f6-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a69f6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a69f6-129">-WhatIf</span></span>
<span data-ttu-id="a69f6-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a69f6-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a69f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69f6-132">CommonParameters</span></span>
<span data-ttu-id="a69f6-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a69f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69f6-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a69f6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69f6-135">입력</span><span class="sxs-lookup"><span data-stu-id="a69f6-135">INPUTS</span></span>

### <span data-ttu-id="a69f6-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a69f6-136">System.String</span></span>

### <span data-ttu-id="a69f6-137">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="a69f6-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a69f6-138">출력</span><span class="sxs-lookup"><span data-stu-id="a69f6-138">OUTPUTS</span></span>

### <span data-ttu-id="a69f6-139">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="a69f6-139">System.Void</span></span>

## <span data-ttu-id="a69f6-140">상속자</span><span class="sxs-lookup"><span data-stu-id="a69f6-140">NOTES</span></span>

## <span data-ttu-id="a69f6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a69f6-141">RELATED LINKS</span></span>

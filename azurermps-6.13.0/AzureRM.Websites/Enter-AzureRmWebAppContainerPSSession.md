---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 350ad76952a2953a107e0626b9cf2e0e8b640bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525895"
---
# <span data-ttu-id="ab356-101">Enter-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="ab356-101">Enter-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="ab356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab356-102">SYNOPSIS</span></span>
<span data-ttu-id="ab356-103">지정한 사이트 또는 슬롯에 지정 된 windows 컨테이너 및 지정 된 리소스 그룹에 원격 PowerShell 세션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab356-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab356-104">SYNTAX</span></span>

### <span data-ttu-id="ab356-105">S1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ab356-105">S1 (Default)</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab356-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="ab356-106">S2</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab356-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ab356-107">DESCRIPTION</span></span>
<span data-ttu-id="ab356-108">지정한 사이트 또는 슬롯에 지정 된 windows 컨테이너 및 지정 된 리소스 그룹에 원격 PowerShell 세션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ab356-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ab356-109">EXAMPLES</span></span>

### <span data-ttu-id="ab356-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab356-110">Example 1</span></span>
```
PS C:\> Enter-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ab356-111">이 명령은 windows 컨테이너 앱 ContosoASP에 대 한 원격 PowerShell 세션을 엽니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="ab356-112">변수</span><span class="sxs-lookup"><span data-stu-id="ab356-112">PARAMETERS</span></span>

### <span data-ttu-id="ab356-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab356-113">-DefaultProfile</span></span>
<span data-ttu-id="ab356-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab356-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ab356-115">-Force</span></span>
<span data-ttu-id="ab356-116">확인 메시지를 표시 하지 않고 PowerShell 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ab356-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ab356-117">-Name</span></span>
<span data-ttu-id="ab356-118">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-118">The name of the web app.</span></span>

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

### <span data-ttu-id="ab356-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab356-119">-PassThru</span></span>
<span data-ttu-id="ab356-120">성공 또는 실패를 나타내는 값 반환</span><span class="sxs-lookup"><span data-stu-id="ab356-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="ab356-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab356-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab356-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab356-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ab356-123">-SlotName</span></span>
<span data-ttu-id="ab356-124">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="ab356-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="ab356-125">-WebApp</span></span>
<span data-ttu-id="ab356-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="ab356-126">The web app object</span></span>

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

### <span data-ttu-id="ab356-127">-확인</span><span class="sxs-lookup"><span data-stu-id="ab356-127">-Confirm</span></span>
<span data-ttu-id="ab356-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab356-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab356-129">-WhatIf</span></span>
<span data-ttu-id="ab356-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab356-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab356-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab356-132">CommonParameters</span></span>
<span data-ttu-id="ab356-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab356-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab356-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab356-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab356-135">입력</span><span class="sxs-lookup"><span data-stu-id="ab356-135">INPUTS</span></span>

### <span data-ttu-id="ab356-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab356-136">System.String</span></span>
### <span data-ttu-id="ab356-137">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="ab356-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="ab356-138">출력</span><span class="sxs-lookup"><span data-stu-id="ab356-138">OUTPUTS</span></span>

### <span data-ttu-id="ab356-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab356-139">System.String</span></span>
## <span data-ttu-id="ab356-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ab356-140">NOTES</span></span>

## <span data-ttu-id="ab356-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab356-141">RELATED LINKS</span></span>

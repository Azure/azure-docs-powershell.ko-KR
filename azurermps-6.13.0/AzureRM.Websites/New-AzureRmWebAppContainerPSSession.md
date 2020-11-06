---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525887"
---
# <span data-ttu-id="91511-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="91511-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="91511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91511-102">SYNOPSIS</span></span>
<span data-ttu-id="91511-103">New-AzureRmWebAppContainerPSSession는 지정 된 사이트 또는 슬롯 및 지정 된 리소스 그룹에서 지정한 windows 컨테이너에 새 원격 PowerShell 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91511-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91511-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91511-104">SYNTAX</span></span>

### <span data-ttu-id="91511-105">S1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="91511-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91511-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="91511-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91511-107">설명은</span><span class="sxs-lookup"><span data-stu-id="91511-107">DESCRIPTION</span></span>
<span data-ttu-id="91511-108">New-AzureRmWebAppContainerPSSession는 지정 된 사이트 또는 슬롯 및 지정 된 리소스 그룹에서 지정한 windows 컨테이너에 새 원격 PowerShell 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91511-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="91511-109">예제의</span><span class="sxs-lookup"><span data-stu-id="91511-109">EXAMPLES</span></span>

### <span data-ttu-id="91511-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="91511-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="91511-111">이렇게 하면 windows 컨테이너 앱 ContosoASP에 새 원격 PowerShell 세션이 생성 되 고 컨테이너에서 실행 중인 프로세스가 표시 됩니다 ContosoASP</span><span class="sxs-lookup"><span data-stu-id="91511-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="91511-112">변수</span><span class="sxs-lookup"><span data-stu-id="91511-112">PARAMETERS</span></span>

### <span data-ttu-id="91511-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91511-113">-DefaultProfile</span></span>
<span data-ttu-id="91511-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91511-115">-Force</span><span class="sxs-lookup"><span data-stu-id="91511-115">-Force</span></span>
<span data-ttu-id="91511-116">확인 메시지를 표시 하지 않고 PowerShell 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91511-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="91511-117">-이름</span><span class="sxs-lookup"><span data-stu-id="91511-117">-Name</span></span>
<span data-ttu-id="91511-118">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-118">The name of the web app.</span></span>

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

### <span data-ttu-id="91511-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91511-119">-ResourceGroupName</span></span>
<span data-ttu-id="91511-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="91511-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="91511-121">-SlotName</span></span>
<span data-ttu-id="91511-122">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91511-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="91511-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="91511-123">-WebApp</span></span>
<span data-ttu-id="91511-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="91511-124">The web app object</span></span>

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

### <span data-ttu-id="91511-125">-확인</span><span class="sxs-lookup"><span data-stu-id="91511-125">-Confirm</span></span>
<span data-ttu-id="91511-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91511-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91511-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91511-127">-WhatIf</span></span>
<span data-ttu-id="91511-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91511-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91511-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91511-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91511-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91511-130">CommonParameters</span></span>
<span data-ttu-id="91511-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91511-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91511-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91511-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91511-133">입력</span><span class="sxs-lookup"><span data-stu-id="91511-133">INPUTS</span></span>

### <span data-ttu-id="91511-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="91511-134">System.String</span></span>
### <span data-ttu-id="91511-135">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="91511-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="91511-136">출력</span><span class="sxs-lookup"><span data-stu-id="91511-136">OUTPUTS</span></span>

### <span data-ttu-id="91511-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="91511-137">System.String</span></span>
## <span data-ttu-id="91511-138">상속자</span><span class="sxs-lookup"><span data-stu-id="91511-138">NOTES</span></span>

## <span data-ttu-id="91511-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91511-139">RELATED LINKS</span></span>

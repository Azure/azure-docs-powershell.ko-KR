---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: c91e5ff71a916e28e199a1c64fde2d69f0193fd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698321"
---
# <span data-ttu-id="9c582-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c582-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="9c582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c582-102">SYNOPSIS</span></span>
<span data-ttu-id="9c582-103">Azure 웹 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="9c582-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c582-104">SYNTAX</span></span>

### <span data-ttu-id="9c582-105">S1</span><span class="sxs-lookup"><span data-stu-id="9c582-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c582-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="9c582-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c582-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9c582-107">DESCRIPTION</span></span>
<span data-ttu-id="9c582-108">**AzWebApp** cmdlet은 리소스 그룹과 웹 앱 이름을 제공 하는 Azure Web app을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="9c582-109">이 cmdlet은 기본적으로 모든 슬롯과 메트릭스도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="9c582-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9c582-110">EXAMPLES</span></span>

### <span data-ttu-id="9c582-111">예제 1: 웹 앱 제거</span><span class="sxs-lookup"><span data-stu-id="9c582-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="9c582-112">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoSite 이라는 Azure Web App을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="9c582-113">변수</span><span class="sxs-lookup"><span data-stu-id="9c582-113">PARAMETERS</span></span>

### <span data-ttu-id="9c582-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c582-114">-AsJob</span></span>
<span data-ttu-id="9c582-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9c582-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c582-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c582-116">-DefaultProfile</span></span>
<span data-ttu-id="9c582-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c582-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9c582-118">-Force</span></span>
<span data-ttu-id="9c582-119">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="9c582-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="9c582-120">-이름</span><span class="sxs-lookup"><span data-stu-id="9c582-120">-Name</span></span>
<span data-ttu-id="9c582-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="9c582-121">WebApp Name</span></span>

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

### <span data-ttu-id="9c582-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c582-122">-ResourceGroupName</span></span>
<span data-ttu-id="9c582-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9c582-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9c582-124">-Web app</span><span class="sxs-lookup"><span data-stu-id="9c582-124">-WebApp</span></span>
<span data-ttu-id="9c582-125">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="9c582-125">WebApp Object</span></span>

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

### <span data-ttu-id="9c582-126">-확인</span><span class="sxs-lookup"><span data-stu-id="9c582-126">-Confirm</span></span>
<span data-ttu-id="9c582-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다. Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c582-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c582-128">-WhatIf</span></span>
<span data-ttu-id="9c582-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c582-130">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c582-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c582-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c582-132">CommonParameters</span></span>
<span data-ttu-id="9c582-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c582-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c582-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c582-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c582-135">입력</span><span class="sxs-lookup"><span data-stu-id="9c582-135">INPUTS</span></span>

### <span data-ttu-id="9c582-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9c582-136">System.String</span></span>

### <span data-ttu-id="9c582-137">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="9c582-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9c582-138">출력</span><span class="sxs-lookup"><span data-stu-id="9c582-138">OUTPUTS</span></span>

### <span data-ttu-id="9c582-139">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="9c582-139">System.Void</span></span>

## <span data-ttu-id="9c582-140">상속자</span><span class="sxs-lookup"><span data-stu-id="9c582-140">NOTES</span></span>

## <span data-ttu-id="9c582-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c582-141">RELATED LINKS</span></span>

[<span data-ttu-id="9c582-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c582-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="9c582-143">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c582-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="9c582-144">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c582-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="9c582-145">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c582-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="9c582-146">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9c582-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



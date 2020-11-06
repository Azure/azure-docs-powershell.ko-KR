---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b903e22a627ca2cb992b179e8f6956d556558b6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536896"
---
# <span data-ttu-id="46500-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46500-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="46500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46500-102">SYNOPSIS</span></span>
<span data-ttu-id="46500-103">Azure 웹 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46500-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46500-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46500-104">SYNTAX</span></span>

### <span data-ttu-id="46500-105">S1</span><span class="sxs-lookup"><span data-stu-id="46500-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46500-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="46500-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46500-107">설명은</span><span class="sxs-lookup"><span data-stu-id="46500-107">DESCRIPTION</span></span>
<span data-ttu-id="46500-108">**AzureRmWebApp** cmdlet은 리소스 그룹과 웹 앱 이름을 제공 하는 Azure Web app을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46500-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="46500-109">이 cmdlet은 기본적으로 모든 슬롯과 메트릭스도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46500-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="46500-110">예제의</span><span class="sxs-lookup"><span data-stu-id="46500-110">EXAMPLES</span></span>

### <span data-ttu-id="46500-111">예제 1: 웹 앱 제거</span><span class="sxs-lookup"><span data-stu-id="46500-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="46500-112">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoSite 이라는 Azure Web App을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46500-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="46500-113">변수</span><span class="sxs-lookup"><span data-stu-id="46500-113">PARAMETERS</span></span>

### <span data-ttu-id="46500-114">-Force</span><span class="sxs-lookup"><span data-stu-id="46500-114">-Force</span></span>
<span data-ttu-id="46500-115">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="46500-115">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="46500-116">-이름</span><span class="sxs-lookup"><span data-stu-id="46500-116">-Name</span></span>
<span data-ttu-id="46500-117">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="46500-117">WebApp Name</span></span>

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

### <span data-ttu-id="46500-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46500-118">-ResourceGroupName</span></span>
<span data-ttu-id="46500-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="46500-119">Resource Group Name</span></span>

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

### <span data-ttu-id="46500-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="46500-120">-WebApp</span></span>
<span data-ttu-id="46500-121">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="46500-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46500-122">-확인</span><span class="sxs-lookup"><span data-stu-id="46500-122">-Confirm</span></span>
<span data-ttu-id="46500-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다. Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46500-123">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46500-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46500-124">-WhatIf</span></span>
<span data-ttu-id="46500-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46500-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46500-126">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46500-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46500-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46500-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46500-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46500-128">-DefaultProfile</span></span>
<span data-ttu-id="46500-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46500-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46500-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46500-130">CommonParameters</span></span>
<span data-ttu-id="46500-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46500-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46500-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46500-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46500-133">입력</span><span class="sxs-lookup"><span data-stu-id="46500-133">INPUTS</span></span>

### <span data-ttu-id="46500-134">Site</span><span class="sxs-lookup"><span data-stu-id="46500-134">Site</span></span>
<span data-ttu-id="46500-135">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46500-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="46500-136">출력</span><span class="sxs-lookup"><span data-stu-id="46500-136">OUTPUTS</span></span>

## <span data-ttu-id="46500-137">상속자</span><span class="sxs-lookup"><span data-stu-id="46500-137">NOTES</span></span>

## <span data-ttu-id="46500-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46500-138">RELATED LINKS</span></span>

[<span data-ttu-id="46500-139">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46500-139">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="46500-140">새로운 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46500-140">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="46500-141">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46500-141">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="46500-142">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46500-142">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="46500-143">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46500-143">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



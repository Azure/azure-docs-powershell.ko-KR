---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 40b14128ec2a1dc48cf098a2c0427728c34c7e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876126"
---
# <span data-ttu-id="03e82-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03e82-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="03e82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e82-102">SYNOPSIS</span></span>
<span data-ttu-id="03e82-103">Azure 웹 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="03e82-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03e82-104">SYNTAX</span></span>

### <span data-ttu-id="03e82-105">S1</span><span class="sxs-lookup"><span data-stu-id="03e82-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03e82-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="03e82-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03e82-107">설명은</span><span class="sxs-lookup"><span data-stu-id="03e82-107">DESCRIPTION</span></span>
<span data-ttu-id="03e82-108">**AzWebApp** cmdlet은 리소스 그룹과 웹 앱 이름을 제공 하는 Azure Web app을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="03e82-109">이 cmdlet은 기본적으로 모든 슬롯과 메트릭스도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="03e82-110">예제의</span><span class="sxs-lookup"><span data-stu-id="03e82-110">EXAMPLES</span></span>

### <span data-ttu-id="03e82-111">예제 1: 웹 앱 제거</span><span class="sxs-lookup"><span data-stu-id="03e82-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="03e82-112">이 명령은 Default-WestUS 이라는 리소스 그룹에 속한 ContosoSite 이라는 Azure Web App을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="03e82-113">변수</span><span class="sxs-lookup"><span data-stu-id="03e82-113">PARAMETERS</span></span>

### <span data-ttu-id="03e82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e82-114">-DefaultProfile</span></span>
<span data-ttu-id="03e82-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e82-116">-Force</span><span class="sxs-lookup"><span data-stu-id="03e82-116">-Force</span></span>
<span data-ttu-id="03e82-117">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="03e82-117">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e82-118">-이름</span><span class="sxs-lookup"><span data-stu-id="03e82-118">-Name</span></span>
<span data-ttu-id="03e82-119">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="03e82-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e82-120">-ResourceGroupName</span></span>
<span data-ttu-id="03e82-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="03e82-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e82-122">-Web app</span><span class="sxs-lookup"><span data-stu-id="03e82-122">-WebApp</span></span>
<span data-ttu-id="03e82-123">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="03e82-123">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03e82-124">-확인</span><span class="sxs-lookup"><span data-stu-id="03e82-124">-Confirm</span></span>
<span data-ttu-id="03e82-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다. Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e82-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e82-126">-WhatIf</span></span>
<span data-ttu-id="03e82-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03e82-128">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03e82-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e82-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03e82-130">-AsJob</span></span>
<span data-ttu-id="03e82-131">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03e82-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e82-132">CommonParameters</span></span>
<span data-ttu-id="03e82-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e82-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e82-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e82-135">입력</span><span class="sxs-lookup"><span data-stu-id="03e82-135">INPUTS</span></span>

### <span data-ttu-id="03e82-136">Site</span><span class="sxs-lookup"><span data-stu-id="03e82-136">Site</span></span>
<span data-ttu-id="03e82-137">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e82-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="03e82-138">출력</span><span class="sxs-lookup"><span data-stu-id="03e82-138">OUTPUTS</span></span>

## <span data-ttu-id="03e82-139">상속자</span><span class="sxs-lookup"><span data-stu-id="03e82-139">NOTES</span></span>

## <span data-ttu-id="03e82-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03e82-140">RELATED LINKS</span></span>

[<span data-ttu-id="03e82-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03e82-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="03e82-142">새로운 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03e82-142">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="03e82-143">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03e82-143">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="03e82-144">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03e82-144">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="03e82-145">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03e82-145">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



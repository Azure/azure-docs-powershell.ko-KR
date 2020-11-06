---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: a3ae7f879827b7b260e60f0d3e0aa70e5a6ab533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528717"
---
# <span data-ttu-id="fbf53-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbf53-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="fbf53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbf53-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf53-103">Azure 웹 앱 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbf53-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbf53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fbf53-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbf53-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fbf53-105">DESCRIPTION</span></span>
<span data-ttu-id="fbf53-106">**AzureRmWebAppSlot** cmdlet은 지정 된 앱 서비스 계획 및 데이터 센터를 사용 하는 지정 된 리소스 그룹에서 Azure 웹 앱 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbf53-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="fbf53-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fbf53-107">EXAMPLES</span></span>

### <span data-ttu-id="fbf53-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbf53-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="fbf53-109">이 명령은 data center ContosoSite에서 Default-WestUS 이라는 기존 리소스 그룹의 기존 웹 앱 이름 아래에 Slot001 라는 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbf53-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="fbf53-110">이 명령은 ContosoServicePlan 이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf53-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="fbf53-111">변수</span><span class="sxs-lookup"><span data-stu-id="fbf53-111">PARAMETERS</span></span>

### <span data-ttu-id="fbf53-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fbf53-112">-AppServicePlan</span></span>
<span data-ttu-id="fbf53-113">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="fbf53-113">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="fbf53-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="fbf53-115">앱 설정이 Hashtable를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf53-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="fbf53-116">-AseName</span></span>
<span data-ttu-id="fbf53-117">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="fbf53-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf53-118">-AseResourceGroupName</span></span>
<span data-ttu-id="fbf53-119">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fbf53-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf53-120">-DefaultProfile</span></span>
<span data-ttu-id="fbf53-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbf53-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="fbf53-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="fbf53-123">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="fbf53-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="fbf53-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="fbf53-125">원본 컨트롤 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="fbf53-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-126">-이름</span><span class="sxs-lookup"><span data-stu-id="fbf53-126">-Name</span></span>
<span data-ttu-id="fbf53-127">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="fbf53-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf53-128">-ResourceGroupName</span></span>
<span data-ttu-id="fbf53-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fbf53-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-130">-슬롯</span><span class="sxs-lookup"><span data-stu-id="fbf53-130">-Slot</span></span>
<span data-ttu-id="fbf53-131">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="fbf53-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="fbf53-132">-SourceWebApp</span></span>
<span data-ttu-id="fbf53-133">원본 Web app 개체</span><span class="sxs-lookup"><span data-stu-id="fbf53-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf53-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbf53-134">-AsJob</span></span>
<span data-ttu-id="fbf53-135">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fbf53-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbf53-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf53-136">CommonParameters</span></span>
<span data-ttu-id="fbf53-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf53-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf53-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf53-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf53-139">입력</span><span class="sxs-lookup"><span data-stu-id="fbf53-139">INPUTS</span></span>

### <span data-ttu-id="fbf53-140">Site</span><span class="sxs-lookup"><span data-stu-id="fbf53-140">Site</span></span>
<span data-ttu-id="fbf53-141">' SourceWebApp ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbf53-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fbf53-142">출력</span><span class="sxs-lookup"><span data-stu-id="fbf53-142">OUTPUTS</span></span>

## <span data-ttu-id="fbf53-143">상속자</span><span class="sxs-lookup"><span data-stu-id="fbf53-143">NOTES</span></span>

## <span data-ttu-id="fbf53-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbf53-144">RELATED LINKS</span></span>

[<span data-ttu-id="fbf53-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbf53-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbf53-146">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbf53-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbf53-147">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbf53-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbf53-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbf53-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbf53-149">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbf53-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbf53-150">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbf53-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbf53-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fbf53-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="fbf53-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fbf53-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: b22dcb6518aa42104a44207e85d02dd7bab914bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526472"
---
# <span data-ttu-id="0654b-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0654b-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="0654b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0654b-102">SYNOPSIS</span></span>
<span data-ttu-id="0654b-103">Azure 웹 앱 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0654b-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0654b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0654b-104">SYNTAX</span></span>

### <span data-ttu-id="0654b-105">S1</span><span class="sxs-lookup"><span data-stu-id="0654b-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0654b-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="0654b-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0654b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0654b-107">DESCRIPTION</span></span>
<span data-ttu-id="0654b-108">**AzureRmWebAppSlot** Cmdlet은 Azure Web App 슬롯에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0654b-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="0654b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0654b-109">EXAMPLES</span></span>

### <span data-ttu-id="0654b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0654b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="0654b-111">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 라는 웹 앱에서 Slot001 라는 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0654b-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0654b-112">변수</span><span class="sxs-lookup"><span data-stu-id="0654b-112">PARAMETERS</span></span>

### <span data-ttu-id="0654b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0654b-113">-DefaultProfile</span></span>
<span data-ttu-id="0654b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0654b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0654b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0654b-115">-Name</span></span>
<span data-ttu-id="0654b-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="0654b-116">WebApp Name</span></span>

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

### <span data-ttu-id="0654b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0654b-117">-ResourceGroupName</span></span>
<span data-ttu-id="0654b-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0654b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0654b-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="0654b-119">-Slot</span></span>
<span data-ttu-id="0654b-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="0654b-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0654b-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="0654b-121">-WebApp</span></span>
<span data-ttu-id="0654b-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="0654b-122">WebApp Object</span></span>

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

### <span data-ttu-id="0654b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0654b-123">CommonParameters</span></span>
<span data-ttu-id="0654b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0654b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0654b-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0654b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0654b-126">입력</span><span class="sxs-lookup"><span data-stu-id="0654b-126">INPUTS</span></span>

### <span data-ttu-id="0654b-127">Site</span><span class="sxs-lookup"><span data-stu-id="0654b-127">Site</span></span>
<span data-ttu-id="0654b-128">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0654b-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0654b-129">출력</span><span class="sxs-lookup"><span data-stu-id="0654b-129">OUTPUTS</span></span>

## <span data-ttu-id="0654b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0654b-130">NOTES</span></span>

## <span data-ttu-id="0654b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0654b-131">RELATED LINKS</span></span>

[<span data-ttu-id="0654b-132">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0654b-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="0654b-133">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0654b-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="0654b-134">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0654b-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="0654b-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0654b-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="0654b-136">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0654b-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="0654b-137">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0654b-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="0654b-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0654b-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: ae97bc08e5ba8c801e3bf5126c6e48dfb7910751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524216"
---
# <span data-ttu-id="4bcd1-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4bcd1-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="4bcd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bcd1-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcd1-103">Azure Web App 인증서 SSL 바인딩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bcd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bcd1-104">SYNTAX</span></span>

### <span data-ttu-id="4bcd1-105">S1</span><span class="sxs-lookup"><span data-stu-id="4bcd1-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bcd1-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="4bcd1-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bcd1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4bcd1-107">DESCRIPTION</span></span>
<span data-ttu-id="4bcd1-108">**AzureRmWebAppSSLBinding** Cmdlet은 Azure Web App에 대 한 SSL (Secure Sockets layer) 바인딩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="4bcd1-109">SSL 바인딩은 웹 앱을 업로드 된 인증서와 연결 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="4bcd1-110">웹 앱은 여러 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="4bcd1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4bcd1-111">EXAMPLES</span></span>

### <span data-ttu-id="4bcd1-112">예제 1: 웹 앱에 대 한 SSL 바인딩 가져오기</span><span class="sxs-lookup"><span data-stu-id="4bcd1-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="4bcd1-113">이 명령은 리소스 그룹 ContosoResourceGroup와 연결 된 웹 앱 ContosoWebApp에 대 한 SSL 바인딩을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="4bcd1-114">예제 2: 웹 앱에 대 한 SSL 바인딩을 가져오려면 개체 참조를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="4bcd1-115">또한이 예제의 명령은 웹 앱 ContosoWebApp SSL 바인딩도 가져옵니다. 그러나이 경우에는 웹 앱 이름 대신 개체 참조와 연결 된 리소스 그룹의 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="4bcd1-116">이 개체 참조는 **AzureRmWebApp** 를 사용 하 여 ContosoWebApp 이라는 웹 앱에 대 한 개체 참조를 만드는 예제에서 첫 번째 명령에 의해 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="4bcd1-117">해당 개체 참조는 $WebApp 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="4bcd1-118">이 변수 및 **AzureRmWebAppSSLBinding** cmdlet은 두 번째 명령에서 SSL 바인딩을 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="4bcd1-119">변수</span><span class="sxs-lookup"><span data-stu-id="4bcd1-119">PARAMETERS</span></span>

### <span data-ttu-id="4bcd1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcd1-120">-DefaultProfile</span></span>
<span data-ttu-id="4bcd1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bcd1-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4bcd1-122">-Name</span></span>
<span data-ttu-id="4bcd1-123">SSL 바인딩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcd1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcd1-124">-ResourceGroupName</span></span>
<span data-ttu-id="4bcd1-125">인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="4bcd1-126">동일한 명령에서 *ResourceGroupName* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="4bcd1-127">-슬롯</span><span class="sxs-lookup"><span data-stu-id="4bcd1-127">-Slot</span></span>
<span data-ttu-id="4bcd1-128">웹 앱 배포 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="4bcd1-129">배포 슬롯을 얻으려면 Get-AzureRMWebAppSlot cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcd1-130">-Web app</span><span class="sxs-lookup"><span data-stu-id="4bcd1-130">-WebApp</span></span>
<span data-ttu-id="4bcd1-131">웹 앱을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-131">Specifies a Web App.</span></span>
<span data-ttu-id="4bcd1-132">웹 앱을 가져오려면 Get-AzureRmWebApp cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

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

### <span data-ttu-id="4bcd1-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="4bcd1-133">-WebAppName</span></span>
<span data-ttu-id="4bcd1-134">이 cmdlet이 SSL 바인딩을 가져오는 웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="4bcd1-135">동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcd1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcd1-136">CommonParameters</span></span>
<span data-ttu-id="4bcd1-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bcd1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcd1-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bcd1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcd1-139">입력</span><span class="sxs-lookup"><span data-stu-id="4bcd1-139">INPUTS</span></span>

### <span data-ttu-id="4bcd1-140">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="4bcd1-140">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="4bcd1-141">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4bcd1-141">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="4bcd1-142">출력</span><span class="sxs-lookup"><span data-stu-id="4bcd1-142">OUTPUTS</span></span>

### <span data-ttu-id="4bcd1-143">Microsoft. Azure. 관리. i m m 네임 스페이스. i m m Namesslstate</span><span class="sxs-lookup"><span data-stu-id="4bcd1-143">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="4bcd1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4bcd1-144">NOTES</span></span>

## <span data-ttu-id="4bcd1-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bcd1-145">RELATED LINKS</span></span>

[<span data-ttu-id="4bcd1-146">새로운 AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4bcd1-146">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="4bcd1-147">제거-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4bcd1-147">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="4bcd1-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4bcd1-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)



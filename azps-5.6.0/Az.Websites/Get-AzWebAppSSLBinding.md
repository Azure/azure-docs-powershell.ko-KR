---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 08a9fbd9798a3fd3b53d7d71aca9ebd607d23164
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973696"
---
# <span data-ttu-id="96d9c-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="96d9c-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="96d9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="96d9c-103">Azure Web App 인증서 SSL 바인딩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="96d9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="96d9c-104">SYNTAX</span></span>

### <span data-ttu-id="96d9c-105">S1</span><span class="sxs-lookup"><span data-stu-id="96d9c-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96d9c-106">S2</span><span class="sxs-lookup"><span data-stu-id="96d9c-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96d9c-107">설명</span><span class="sxs-lookup"><span data-stu-id="96d9c-107">DESCRIPTION</span></span>
<span data-ttu-id="96d9c-108">**Get-AzWebAppSSLBinding** cmdlet은 Azure Web App에 Secure Sockets Layer(SSL) 바인딩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="96d9c-109">SSL 바인딩은 웹앱을 업로드된 인증서와 연결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="96d9c-110">Web Apps는 여러 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="96d9c-111">예제</span><span class="sxs-lookup"><span data-stu-id="96d9c-111">EXAMPLES</span></span>

### <span data-ttu-id="96d9c-112">예제 1: 웹앱에 대한 SSL 바인딩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="96d9c-113">이 명령은 리소스 그룹 ContosoResourceGroup과 연결된 Web App ContosoWebApp에 대한 SSL 바인딩을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="96d9c-114">예제 2: 개체 참조를 사용하여 Web App에 대한 SSL 바인딩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="96d9c-115">이 예제의 명령은 Web App ContosoWebApp에 대한 SSL 바인딩도 제공합니다. 그러나 이 경우 웹앱 이름과 연결된 리소스 그룹의 이름 대신 개체 참조가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="96d9c-116">이 개체 참조는 **Get-AzWebApp을** 사용하여 ContosoWebApp이라는 웹앱에 대한 개체 참조를 만드는 예제의 첫 번째 명령에 의해 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="96d9c-117">해당 개체 참조는 이라는 변수에 $WebApp.</span><span class="sxs-lookup"><span data-stu-id="96d9c-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="96d9c-118">이 변수와 **Get-AzWebAppSSLBinding** cmdlet은 두 번째 명령에서 SSL 바인딩을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="96d9c-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="96d9c-119">PARAMETERS</span></span>

### <span data-ttu-id="96d9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d9c-120">-DefaultProfile</span></span>
<span data-ttu-id="96d9c-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96d9c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="96d9c-122">-Name</span></span>
<span data-ttu-id="96d9c-123">SSL 바인딩의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="96d9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="96d9c-125">인증서가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="96d9c-126">동일한 명령에서 *ResourceGroupName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="96d9c-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="96d9c-127">-Slot</span></span>
<span data-ttu-id="96d9c-128">웹앱 배포 슬롯을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="96d9c-129">배포 슬롯을 얻은 경우 Get-AzWebAppSlot cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="96d9c-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="96d9c-130">-WebApp</span></span>
<span data-ttu-id="96d9c-131">웹앱을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-131">Specifies a Web App.</span></span>
<span data-ttu-id="96d9c-132">웹앱을 얻으면 Get-AzWebApp cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="96d9c-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="96d9c-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="96d9c-133">-WebAppName</span></span>
<span data-ttu-id="96d9c-134">이 cmdlet에서 SSL 바인딩을 얻게 하는 웹앱 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="96d9c-135">동일한 명령에서 *WebAppName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="96d9c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d9c-136">CommonParameters</span></span>
<span data-ttu-id="96d9c-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96d9c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d9c-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96d9c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d9c-139">입력</span><span class="sxs-lookup"><span data-stu-id="96d9c-139">INPUTS</span></span>

### <span data-ttu-id="96d9c-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="96d9c-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="96d9c-141">출력</span><span class="sxs-lookup"><span data-stu-id="96d9c-141">OUTPUTS</span></span>

### <span data-ttu-id="96d9c-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="96d9c-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="96d9c-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96d9c-143">NOTES</span></span>

## <span data-ttu-id="96d9c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96d9c-144">RELATED LINKS</span></span>

[<span data-ttu-id="96d9c-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="96d9c-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="96d9c-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="96d9c-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="96d9c-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="96d9c-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



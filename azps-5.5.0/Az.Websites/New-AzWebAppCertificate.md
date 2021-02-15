---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 56f8d69325e5a7918668ac2807449f348e73c91b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182449"
---
# <span data-ttu-id="555e6-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="555e6-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="555e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="555e6-102">SYNOPSIS</span></span>
<span data-ttu-id="555e6-103">Azure Web App에 대한 App Service 관리 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="555e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="555e6-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="555e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="555e6-105">DESCRIPTION</span></span>
<span data-ttu-id="555e6-106">**New-AzWebAppCertificate** cmdlet은 Azure App Service 관리 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="555e6-107">예제</span><span class="sxs-lookup"><span data-stu-id="555e6-107">EXAMPLES</span></span>

### <span data-ttu-id="555e6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="555e6-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="555e6-109">이 명령은 주어진 WebApp에 대한 App Service 관리 인증서를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="555e6-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="555e6-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="555e6-111">이 명령은 App Service 관리 인증서를 만들고 주어진 WebApp 슬롯에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="555e6-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="555e6-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="555e6-113">이 명령은 App Service 관리 인증서를 만들고 주어진 WebApp에 바인딩합니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="555e6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="555e6-114">PARAMETERS</span></span>

### <span data-ttu-id="555e6-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="555e6-115">-AddBinding</span></span>
<span data-ttu-id="555e6-116">만든 인증서를 WebApp/slot에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-116">To add the created certificate to WebApp/slot.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555e6-117">-DefaultProfile</span></span>
<span data-ttu-id="555e6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e6-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="555e6-119">-HostName</span></span>
<span data-ttu-id="555e6-120">웹앱/슬롯과 연결된 사용자 지정 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-120">Custom hostnames associated with web app/slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="555e6-121">-Name</span></span>
<span data-ttu-id="555e6-122">인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-122">The name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="555e6-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="555e6-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="555e6-125">-Slot</span></span>
<span data-ttu-id="555e6-126">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-126">The name of the web app slot.</span></span>

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

### <span data-ttu-id="555e6-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="555e6-127">-SslState</span></span>
<span data-ttu-id="555e6-128">Ssl 상태 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-128">Ssl state option.</span></span>
<span data-ttu-id="555e6-129">'SniEnabled' 또는 'IpBasedEnabled'를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="555e6-130">기본 옵션은 'SniEnabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-130">Default option is 'SniEnabled'.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e6-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="555e6-131">-WebAppName</span></span>
<span data-ttu-id="555e6-132">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-132">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555e6-133">CommonParameters</span></span>
<span data-ttu-id="555e6-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="555e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555e6-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="555e6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555e6-136">입력</span><span class="sxs-lookup"><span data-stu-id="555e6-136">INPUTS</span></span>

### <span data-ttu-id="555e6-137">없음</span><span class="sxs-lookup"><span data-stu-id="555e6-137">None</span></span>

## <span data-ttu-id="555e6-138">출력</span><span class="sxs-lookup"><span data-stu-id="555e6-138">OUTPUTS</span></span>

### <span data-ttu-id="555e6-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="555e6-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="555e6-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="555e6-140">NOTES</span></span>

## <span data-ttu-id="555e6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="555e6-141">RELATED LINKS</span></span>
[<span data-ttu-id="555e6-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="555e6-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)
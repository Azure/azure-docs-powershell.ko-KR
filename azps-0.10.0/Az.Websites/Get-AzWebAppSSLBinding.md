---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876149"
---
# <span data-ttu-id="7e295-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7e295-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="7e295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e295-102">SYNOPSIS</span></span>
<span data-ttu-id="7e295-103">Azure Web App 인증서 SSL 바인딩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="7e295-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e295-104">SYNTAX</span></span>

### <span data-ttu-id="7e295-105">S1</span><span class="sxs-lookup"><span data-stu-id="7e295-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e295-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="7e295-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e295-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7e295-107">DESCRIPTION</span></span>
<span data-ttu-id="7e295-108">**AzWebAppSSLBinding** Cmdlet은 Azure Web App에 대 한 SSL (Secure Sockets layer) 바인딩을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="7e295-109">SSL 바인딩은 웹 앱을 업로드 된 인증서와 연결 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="7e295-110">웹 앱은 여러 인증서에 바인딩할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="7e295-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7e295-111">EXAMPLES</span></span>

### <span data-ttu-id="7e295-112">예제 1: 웹 앱에 대 한 SSL 바인딩 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e295-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="7e295-113">이 명령은 리소스 그룹 ContosoResourceGroup와 연결 된 웹 앱 ContosoWebApp에 대 한 SSL 바인딩을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="7e295-114">예제 2: 웹 앱에 대 한 SSL 바인딩을 가져오려면 개체 참조를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="7e295-115">또한이 예제의 명령은 웹 앱 ContosoWebApp SSL 바인딩도 가져옵니다. 그러나이 경우에는 웹 앱 이름 대신 개체 참조와 연결 된 리소스 그룹의 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="7e295-116">이 개체 참조는 **AzWebApp** 를 사용 하 여 ContosoWebApp 이라는 웹 앱에 대 한 개체 참조를 만드는 예제에서 첫 번째 명령에 의해 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="7e295-117">해당 개체 참조는 $WebApp 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="7e295-118">이 변수 및 **AzWebAppSSLBinding** cmdlet은 두 번째 명령에서 SSL 바인딩을 가져오는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="7e295-119">변수</span><span class="sxs-lookup"><span data-stu-id="7e295-119">PARAMETERS</span></span>

### <span data-ttu-id="7e295-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e295-120">-DefaultProfile</span></span>
<span data-ttu-id="7e295-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e295-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7e295-122">-Name</span></span>
<span data-ttu-id="7e295-123">SSL 바인딩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="7e295-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e295-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e295-125">인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="7e295-126">동일한 명령에서 *ResourceGroupName* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="7e295-127">-슬롯</span><span class="sxs-lookup"><span data-stu-id="7e295-127">-Slot</span></span>
<span data-ttu-id="7e295-128">웹 앱 배포 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="7e295-129">배포 슬롯을 얻으려면 Get-AzWebAppSlot cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e295-130">-Web app</span><span class="sxs-lookup"><span data-stu-id="7e295-130">-WebApp</span></span>
<span data-ttu-id="7e295-131">웹 앱을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-131">Specifies a Web App.</span></span>
<span data-ttu-id="7e295-132">웹 앱을 가져오려면 Get-AzWebApp cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="7e295-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7e295-133">-WebAppName</span></span>
<span data-ttu-id="7e295-134">이 cmdlet이 SSL 바인딩을 가져오는 웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="7e295-135">동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e295-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e295-136">CommonParameters</span></span>
<span data-ttu-id="7e295-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e295-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e295-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e295-139">입력</span><span class="sxs-lookup"><span data-stu-id="7e295-139">INPUTS</span></span>

### <span data-ttu-id="7e295-140">Site</span><span class="sxs-lookup"><span data-stu-id="7e295-140">Site</span></span>
<span data-ttu-id="7e295-141">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e295-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7e295-142">출력</span><span class="sxs-lookup"><span data-stu-id="7e295-142">OUTPUTS</span></span>

## <span data-ttu-id="7e295-143">상속자</span><span class="sxs-lookup"><span data-stu-id="7e295-143">NOTES</span></span>

## <span data-ttu-id="7e295-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e295-144">RELATED LINKS</span></span>

[<span data-ttu-id="7e295-145">새로운 AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7e295-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="7e295-146">제거-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7e295-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="7e295-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e295-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



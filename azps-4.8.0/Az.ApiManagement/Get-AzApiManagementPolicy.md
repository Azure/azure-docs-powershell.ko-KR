---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 24af453d6605bc42e8c504cef26d368369753d9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048016"
---
# <span data-ttu-id="fc328-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fc328-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="fc328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc328-102">SYNOPSIS</span></span>
<span data-ttu-id="fc328-103">지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="fc328-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc328-104">SYNTAX</span></span>

### <span data-ttu-id="fc328-105">GetTenantLevel (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc328-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc328-106">Get제품 수준</span><span class="sxs-lookup"><span data-stu-id="fc328-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc328-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="fc328-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc328-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="fc328-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc328-109">설명은</span><span class="sxs-lookup"><span data-stu-id="fc328-109">DESCRIPTION</span></span>
<span data-ttu-id="fc328-110">**AzApiManagementPolicy** cmdlet은 지정 된 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="fc328-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fc328-111">EXAMPLES</span></span>

### <span data-ttu-id="fc328-112">예제 1: 테 넌 트 수준 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc328-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="fc328-113">이 명령은 테 넌 트 수준 정책을 가져와 tenantpolicy.xml 라는 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="fc328-114">예제 2: 제품 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc328-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="fc328-115">이 명령은 제품 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="fc328-116">예제 3: API 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc328-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="fc328-117">이 명령은 API 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="fc328-118">예제 4: 작업 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc328-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="fc328-119">이 명령은 작업 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="fc328-120">예제 5: RawXml 형식으로 테 넌 트 범위 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc328-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $apimContext -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="fc328-121">이 명령은 비 Xml 이스케이프 형식의 테 넌 트 범위 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="fc328-122">변수</span><span class="sxs-lookup"><span data-stu-id="fc328-122">PARAMETERS</span></span>

### <span data-ttu-id="fc328-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fc328-123">-ApiId</span></span>
<span data-ttu-id="fc328-124">기존 API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="fc328-125">이 매개 변수를 지정 하면 cmdlet이 API 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc328-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="fc328-126">-ApiRevision</span></span>
<span data-ttu-id="fc328-127">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-127">Identifier of API Revision.</span></span> <span data-ttu-id="fc328-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-128">This parameter is optional.</span></span> <span data-ttu-id="fc328-129">지정 하지 않으면 현재 활성 api 개정판에서 정책이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc328-130">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fc328-130">-Context</span></span>
<span data-ttu-id="fc328-131">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-131">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc328-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc328-132">-DefaultProfile</span></span>
<span data-ttu-id="fc328-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc328-134">-Force</span><span class="sxs-lookup"><span data-stu-id="fc328-134">-Force</span></span>
<span data-ttu-id="fc328-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="fc328-135">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc328-136">-형식</span><span class="sxs-lookup"><span data-stu-id="fc328-136">-Format</span></span>
<span data-ttu-id="fc328-137">API 관리 정책의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="fc328-138">이 매개 변수의 기본값은 "xml"입니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-138">The default value for this parameter is "xml".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc328-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fc328-139">-OperationId</span></span>
<span data-ttu-id="fc328-140">기존 API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="fc328-141">*Apiid* 에이 매개 변수를 지정 하는 경우 cmdlet은 작업 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc328-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="fc328-142">-ProductId</span></span>
<span data-ttu-id="fc328-143">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="fc328-144">이 매개 변수를 지정 하는 경우 cmdlet은 제품 범위 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc328-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="fc328-145">-SaveAs</span></span>
<span data-ttu-id="fc328-146">결과를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="fc328-147">이 매개 변수를 지정 하지 않으면 결과는 sting로 파이프라인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc328-148">-확인</span><span class="sxs-lookup"><span data-stu-id="fc328-148">-Confirm</span></span>
<span data-ttu-id="fc328-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc328-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc328-150">-WhatIf</span></span>
<span data-ttu-id="fc328-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc328-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc328-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc328-153">CommonParameters</span></span>
<span data-ttu-id="fc328-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc328-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc328-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc328-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc328-156">입력</span><span class="sxs-lookup"><span data-stu-id="fc328-156">INPUTS</span></span>

### <span data-ttu-id="fc328-157">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fc328-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fc328-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc328-158">System.String</span></span>

### <span data-ttu-id="fc328-159">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc328-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc328-160">출력</span><span class="sxs-lookup"><span data-stu-id="fc328-160">OUTPUTS</span></span>

### <span data-ttu-id="fc328-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc328-161">System.String</span></span>

## <span data-ttu-id="fc328-162">상속자</span><span class="sxs-lookup"><span data-stu-id="fc328-162">NOTES</span></span>

## <span data-ttu-id="fc328-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc328-163">RELATED LINKS</span></span>

[<span data-ttu-id="fc328-164">제거-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fc328-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="fc328-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fc328-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


